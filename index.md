---
layout: default
title: ""
---


## Contents

More structured. Chronological.

<nav class="toc">
{% for folder_name in site.config.collection_order %}
  {% assign collection = site.collections[folder_name] %}
  {% if collection %}
    <strong>{{ folder_name | replace:'_',' ' | capitalize }}</strong>
    <ul>
      {% assign sorted = collection.docs | sort: "weight" %}
      {% for doc in sorted %}
        {% if doc.basename != "index" %}
          <li><a href="{{ doc.url }}">{{ doc.title }}</a></li>
        {% endif %}
      {% endfor %}
    </ul>
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
