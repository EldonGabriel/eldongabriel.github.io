---
layout: default
title: Reports
permalink: /posts/
---
<h1>Reports</h1>

{% for post in site.posts %}
  <h2>{{ post.title }}</h2>
  
  <p><strong>Categories:</strong>
    {% for category in post.categories %}
      {{ category }}
    {% endfor %}
  </p>

  <p>{{ post.excerpt }}</p>
{% endfor %}
