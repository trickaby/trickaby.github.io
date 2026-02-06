---
layout: default
title: ""
---


## Contents

More structured. Chronological.

<nav class="toc">
{% assign pages_nav = site.pages | where:"nav",true | sort:"path" %}

{% assign last_folder = "" %}

<ul>
{% for p in pages_nav %}
  {% assign parts = p.path | split:'/' %}
  {% assign folder = parts[1] %}
  {% assign file = parts | last %}

    {% if folder != last_folder and folder != "" %}
    {% if forloop.index != 1 %}
    </ul></li>
    {% endif %}
    <li>
    {% assign folder_index = site.pages | where:"path","_pages/" | where:"basename",folder | first %}
    {% if folder_index %}
    <strong><a href="{{ folder_index.url }}">{{ folder | replace:'_',' ' | capitalize }}</a></strong>
    {% else %}
    <strong>{{ folder | replace:'_',' ' | capitalize }}</strong>
    {% endif %}
    <ul>
    {% assign last_folder = folder %}
    {% endif %}
    
    {% if file != "index.md" %}
    <li><a href="{{ p.url }}">{{ p.title }}</a></li>
    {% endif %}
    
    {% if forloop.last %}
    </ul></li>
    {% endif %}
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
