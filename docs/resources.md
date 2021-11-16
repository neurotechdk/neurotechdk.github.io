---
title: Resources
layout: default
permalink: /resources
---


{% assign r_grouped = site.resource | group_by: 'resource_type' %}
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
