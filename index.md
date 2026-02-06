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
    {% comment %} Determine folder header title {% endcomment %}
    {% assign index_doc = collection.docs | where:"basename","index" | first %}
    {% if index_doc %}
      <strong><a href="{{ index_doc.url }}">{{ index_doc.title }}</a></strong>
    {% else %}
      <strong>{{ folder_name | replace:'_',' ' | capitalize }}</strong>
    {% endif %}

    <ul>
      {% assign sorted_docs = collection.docs | sort: "weight" %}
      {% for doc in sorted_docs %}
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
