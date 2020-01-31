---
layout: default
title: Projects
permalink: /projects/
---
<h1>{{ page.title }}</h1>
*Because nothing is like pratice*

I am challenging myself to do some Pocs with different technologies!
{% for category in site.categories %}
{% if category[0] == "projects" %}
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endif %}
{% endfor %}
