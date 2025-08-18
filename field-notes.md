---
layout: default
title: Field Notes
permalink: /field-notes/
---
<h1>Field Notes</h1>

<ul>
  {% for post in site.posts %}
    {% if post.categories contains "field-notes" %}
      <li>
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p>{{ post.excerpt }}</p>
      </li>
    {% endif %}
  {% endfor %}
</ul>

{% assign field_notes_posts = site.posts | where:"tags","field-notes" %}
{% for post in field_notes_posts %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
