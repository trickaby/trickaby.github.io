---
layout: default
title: ""
---

Welcome to my page. At the moment it's being used to document Japan travels. Anything I share I'll post links to here.

Current plan is for posts to just be mad ramblings without much structure that probably aren't worth reading. 
The organised pages will be more informative and travel focussed, also probably not worth reading.

If I decide to share photos or videos, I'll post links here too, they'll probably be hosted away from this site. 
Those familiar with my work as a photographer will know they won't be worth seeing


<hr>


## Contents

More structured. Chronological.


- [pre travel](/0-pre-travel)
- Hokkaido
	- [Arrival](/hokkaido/1-arrival/)
	- [Noboribetsu](/hokkaido/Noboribetsu Onsen)


<hr>

## Posts

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
