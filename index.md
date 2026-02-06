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
[Arrival](/hokkaido/1-arrival.md)
</ul>

<!-- Manual header -->
<strong>Spring Travels</strong>
<!-- Any other single pages -->
<strong>Other Pages</strong>


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
