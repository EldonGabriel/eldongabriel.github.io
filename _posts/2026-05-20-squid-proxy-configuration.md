---
title: "REPORT – Linux Admin: Squid Proxy Configuration & Authentication – v1.0.0"
date: 2026-05-20
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Linux, Squid Proxy, Access Control, Authentication, Security Hardening, System Administration]
excerpt: "Technical implementation of a secure, authenticated Squid proxy server with domain-level web filtering."
image:
  path: /assets/images/posts/Squid.png
  thumbnail: /assets/images/posts/Squid.png
---

# 0.0 Executive Summary

This report documents the deployment, configuration, and validation of an authenticated Squid Proxy server on an Ubuntu system. The primary objective was to build a secure gateway that restricts outbound web traffic based on domain names and requires user authentication.

The implementation involved installing the Squid daemon, setting up a secure user credentials database, and establishing strict Access Control Lists (ACLs). Access rules were systematically arranged to deny unauthorized destinations while permitting verified users to connect to safe and approved domains.

The result was a fully functional security gateway. Testing confirmed that unauthenticated traffic was blocked, unauthorized websites were restricted, and valid credentials granted filtered Internet access. This setup provides an essential layer of defensive architecture by improving network visibility and stopping unwanted outbound communication.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 Squid Proxy Configuration & Authentication

## 1.1 Project Description

The goal of this task was to develop practical skills in egress traffic filtering by deploying a proxy server. This architecture ensures that local users cannot connect directly to the Internet without passing through the centralized security control points.

This implementation demonstrates the following:

- **Proxy Daemon Deployment:** Installation and management of the core Squid service.
- **Identity Enforcement:** Configuring basic authentication with encrypted passwords using `htpasswd`.
- **Egress Web Filtering:** Restricting web access to specific approved domains while blocking all others by default.
- **Access Rule Strategy:** Setting up rules where blocking actions occur before allowing actions to prevent security bypasses.

---

## 1.2 Technical Execution

### 1.2.1 Installation and Basic Setup

- **Service Installation:** The Squid proxy package was installed using a system package manager. The core configuration file is located at `/etc/squid/squid.conf`.
- **Port Assignment:** The service was configured to listen on the standard proxy port `3128`.

### 1.2.2 Authentication and ACL Setup

- **Credentials Database:** Created a secure password file at `/etc/squid/passwd` using the `htpasswd` utility. This utility ensures that passwords are encrypted using secure algorithms rather than being stored in plain text.
- **External ACL Files:** Built text files to hold lists of web domains for easier management of the data. An external file was created at `/etc/squid/allowed_domains.txt` to store the list of approved web pages.
- **Rule Order Implementation:** The `squid.conf` file was configured to process checks in a strict sequence:
    1. Define the authentication program helper path.
    2. Read the external domain lists.
    3. Block traffic that fails authentication.
    4. Block traffic attempting to reach unapproved domains.
    5. Traffic is permitted only after authentication and domain validation checks are successful.

```bash
# Example ACL enforcement structure inside squid.conf
acl authenticated_users proxy_auth REQUIRED
acl allowed_sites dstdomain "/etc/squid/allowed_domains.txt"

http_access deny !authenticated_users
http_access allow allowed_sites
http_access deny all
```


 
### Key Insight

The order of the proxy access rules is critical. Placing a global allow rule above a specific deny rule completely bypasses the security restrictions. Rules must always flow from specific restrictions to broad permissions, ending in a default deny-all state.



## 1.3 Validation and Testing

A structured troubleshooting and validation process was executed across multiple system layers to confirm the correct operation.

- **Service Validation:** Confirmed Squid was active and listening on port `3128`
- **Authentication Testing:** Verified proxy returns HTTP `407 Proxy Authentication Required` without credentials.
- **Domain Filtering Proof:** Confirmed blocked domains return HTTP `403 Forbidden` when not in allow list.
- **Log Analysis:** Verified `/var/log/squid/access.log` records user activity, destinations, and actions (`TCP_DENIED` or `TCP_MISS`).

## 1.4 Troubleshooting Highlights

- **Missing Dot Trap:** Omitting a leading dot (e.g., `google.com` instead of `.google.com`) allowed subdomains to bypass filtering. The ACL was updated to include proper domain scoping.
- **Syntax Validation Errors:** A typographical error in the authentication helper path caused a configuration failure. The issue was resolved through configuration validation prior to service restart.

### Tool Mapping

| Function | Native Command / Path | Verification Indicator |
| :--- | :--- | :--- |
| **Credential Storage** | `htpasswd -c /etc/squid/passwd` | Encrypted credential string generation |
| **Configuration Audit** | `/etc/squid/squid.conf` | Validation of ACL order logic |
| **Log Monitoring** | `tail -f /var/log/squid/access.log` | Real-time tracking of HTTP 407/403 responses |
| **Connection Testing** | `curl -x http://user:pass@IP:3128` | Verification of filtered payload delivery |

 
# 2.0 CONCLUSION

## 2.1 Key Takeaways

- Proxy servers centralize and control outbound internet traffic.
- External ACL files improve maintainability by separating rules from configuration.
- Authentication enforces user accountability and removes anonymous access.
- Log inspection is critical for validating policy enforcement.

## 2.2 Security Implications and Recommendations

**Risk: Unrestricted Egress Communication**  
Without outbound controls, compromised systems may communicate with external infrastructure undetected.

**Mitigation:**
- Deploy authenticated proxy services as a default network control point.
- Enforce a default deny rule for all non-proxied traffic.

**Risk: Credential Exposure**  
Storing credentials in plain text increases the risk of unauthorized access and account compromise if files are exposed.

**Mitigation:**
- Use secure hashing via `htpasswd` for all credentials.
- Restrict access to `/etc/squid/passwd` to the proxy service account.

**Best Practices**
- Place deny rules above allow rules in all ACL configurations.
- Use change management when modifying allowed domain lists.
- Validate configuration syntax before applying changes to production.

**Framework Alignment**
- **NIST CSF (DE.CM):** Monitoring of outbound connections for anomalies.
- **CIS Control 12:** Network infrastructure control and boundary enforcement.
- **ISO 27001 (A.12.1.3):** Operational procedures for system protection and access control.
