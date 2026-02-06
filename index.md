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
[[1-arrival]]
</ul>

<!-- Manual header -->
<strong>Spring Travels</strong>
<ul>
[[Temp]]
</ul>

<!-- Any other single pages -->
<strong>Other Pages</strong>
<ul>
[[0-pre-travel]]
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
