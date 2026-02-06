---
layout: default
title: ""
---



<nav class="toc">
{% assign nav_pages = site.pages | where: "nav", true | sort: "path" %}
{% for p in nav_pages %}
  <a href="{{ p.url }}">{{ p.title }}</a><br>
{% endfor %}
</nav>

<hr>

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
