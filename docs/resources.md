---
title: Resources
layout: default
permalink: /resources
---


{% assign r_grouped = site.posts | group_by: 'author' %}
{% for group in r_grouped %}
  <h5>{{group.name}}</h5>  
  <ul>
  {% for r in group.items %}
    <li>
      <a href="{{ r.url }}">
        {{ r.title }}
      </a>
    </li>
  {% endfor %}
  </ul>
{% endfor %}
