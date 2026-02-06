---
layout: default
title: ""
---


## Contents

More structured. Chronological.

<nav class="toc">

<!-- Manual header -->
<strong>Hokkaido</strong>
<ul>
{% assign hokkaido_pages = site.pages | where_exp:"p","p.path contains '_pages/hokkaido/'" | sort: "weight" %}
{% for p in hokkaido_pages %}
  <li><a href="{{ p.url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>

<!-- Manual header -->
<strong>Spring Travels</strong>
<ul>
{% assign spring_pages = site.pages | where_exp:"p","p.path contains '_pages/spring_travels/'" | sort: "weight" %}
{% for p in spring_pages %}
  <li><a href="{{ p.url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>

<!-- Any other single pages -->
<strong>Other Pages</strong>
<ul>
{% assign other_pages = site.pages | where_exp:"p","p.path contains '_pages/' and p.path contains '/' == false" | sort:"weight" %}
{% for p in other_pages %}
  <li><a href="{{ p.url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>

</nav>





<hr>

## Posts

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
