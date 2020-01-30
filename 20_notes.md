---
layout: default
title: Notes
permalink: /notes/
---
<h1>{{ page.title }}</h1>
{% for category in site.categories %}
{% if category[0] == "notes" %}
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endif %}
{% endfor %}
