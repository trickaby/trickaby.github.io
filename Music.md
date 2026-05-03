---
layout: default
title: Music
permalink: /music
---

I've been meaning to do something music related. Initially I thought I'd do a little song of the day/week to give a little indication of what I'm listening to and what I like. It didn't end up happening but I'd still like to do something. I'll try doing a playlist of sorts, with a little post attached detailing why I like it. I'll just post youtube links, I don't use spotify (and neither should you!).

I'm not sure if I should separate them into separate posts, or just make this one long page. We'll see.

If anything catches your ear, please do let me know. I tend to feel like I force my taste in music onto people a lot, so it would be nice if some stuff is actually appreciated and enjoyed.

<ul>
{% for post in site.music%}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>

{% assign music_pages = site.pages | where_exp: "page", "page.path contains '_music/'" %}

{% for page in music_pages %}
- [{{ page.title }}]({{ page.url }})
{% endfor %}