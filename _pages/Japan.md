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


This is everything post-spring travels. From April onwards, where I spent 6 months studying Japanese in Tokyo. Then a month or so of me being a tourist again.

<ul>
{% assign japan_posts = site.posts
  | where_exp: "post", "post.path contains '_posts/japan/'"
  | reverse %}

{% for post in japan_posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>