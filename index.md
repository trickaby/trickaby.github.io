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


#### [Photos](/Photos)

<hr>

- [pre travel](/0-pre-travel)
- [Hokkaido](/hokkaido)
	- [Arrival](/hokkaido/1-arrival/)
	- [Noboribetsu](/hokkaido/Noboribetsu Onsen)
	- [Onsen 2](/hokkaido/Onsen 2)
- Spring travels
	- [Kyoto](/spring_travels/Kyoto)
		- [Start](/spring_travels/Start)
		- [Day 1](spring_travels/Kyoto/Day 1 Kyoto)
		- [Day 2](spring_travels/Kyoto/Day 2 Kyoto)
		- [Day 3](spring_travels/Kyoto/Day 3 Kyoto)
	- [Osaka](/spring_travels/Osaka)
		- [To Osaka](/spring_travels/Osaka/To Osaka)
		- [Day 2](/spring_travels/Osaka/Osaka day 2)
		- [Day 3](/spring_travels/Osaka/Osaka day 3)
		- [Day trip to Kobe!](/spring_travels/Osaka/Day trip to Kobe!)
	- [Onomichi](/spring_travels/Onomichi)
		- [To Onomichi](/spring_travels/Onomichi/To Onomichi)
		- [Cycling the Shimanami Kaido](/spring_travels/Onomichi/Cycling the Shimanami Kaido)
		- [Returning from Imabari](spring_travels/Onomichi/Returning from Imabari)
	- [Hiroshima](/spring_travels/Hiroshima)
		- [To Hiroshima](/spring_travels/Hiroshima/To Hiroshima)
		- [Day 2](/spring_travels/Hiroshima/Hiroshima day 2)
	- [Ube](/spring_travels/Ube)
		- [To Ube](/spring_travels/Ube/To Ube)
		- [Day 2](/spring_travels/Ube/Ube day 2)
		- [Day 3](/spring_travels/Ube/Ube day 3)
	- [Yokohama](/spring_travels/Yokohama)
		- [To Yokohama](/spring_travels/Yokohama/To Yokohama)

<hr>

## Posts

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
