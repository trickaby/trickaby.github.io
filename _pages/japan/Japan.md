---
layout: default
title: Photos
---

- [pre travel](/0-pre-travel)
- [Hokkaido](/hokkaido)
    - [Arrival](/hokkaido/1-arrival/)
    - [Noboribetsu](/hokkaido/Noboribetsu Onsen)
    - [Onsen 2](/hokkaido/Onsen 2)
- [Spring travels](/spring_travels)

<hr>

## Posts

<ul>
{% assign main_posts = site.posts
  | where_exp: "post", "post.path contains '_posts/main/'"
  | reverse %}

{% for post in main_posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>