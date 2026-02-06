---
layout: default
title: ""
---


## Contents

More structured. Chronological.

<nav class="toc">
{% assign pages = site.pages | where:"nav",true | sort:"path" %}

{% assign current_folder = "" %}

<ul>
{% for p in pages %}
  {% assign parts = p.path | split:'/' %}
  {% assign folder = parts[1] %}
  {% assign file = parts | last %}

    {% if folder != current_folder %}
        {% if folder != file %}
            {% if forloop.index != 1 %}
                </ul>  <!-- close previous folder list -->
            {% endif %}
            <li><strong>{{ folder | replace:'_',' ' }}</strong>
                <ul>
        {% endif %}
        {% assign current_folder = folder %}
    {% endif %}

    {% if parts.size > 1 and file != 'index.md' %}
        <li><a href="{{ p.url }}">{{ p.title }}</a></li>
    {% elsif file != 'index.md' %}
        <li><a href="{{ p.url }}">{{ p.title }}</a></li>
    {% endif %}

    {% if forloop.last %}
            </ul>
        </li>
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
