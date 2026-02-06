---
layout: default
title: ""
---


## Contents

More structured. Chronological.

<nav class="toc">
{% assign pages = site.pages | where:"nav",true | sort:"path" %}

{% assign last_folder = "" %}

{% for p in pages %}

    {% assign parts = p.path | split:'/' %}
    {% assign folder = parts[0] %}
    {% assign file = parts | last %}

    {% if folder != last_folder %}
        {% if folder != file %}
            <strong>{{ folder | replace:'_',' ' }}</strong><br>
        {% endif %}
    {% assign last_folder = folder %}
{% endif %}

{% if parts.size > 1 and file != 'index.md' %}
    &nbsp;&nbsp;&nbsp;<a href="{{ p.url }}">{{ p.title }}</a><br>
{% elsif file != 'index.md' %}
    <a href="{{ p.url }}">{{ p.title }}</a><br>
{% endif %}

{% endfor %}
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
