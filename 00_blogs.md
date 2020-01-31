---
layout: default
title: Blog
permalink: /blogs/
---
<h1>{{ page.title }}</h1>
{% for category in site.categories %}
{% if category[0] == "blogs" %}
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endif %}
{% endfor %}
