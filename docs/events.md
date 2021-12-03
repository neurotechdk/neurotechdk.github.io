---
title: Resources
layout: default
permalink: /events
---


{% assign e_grouped = site.event | group_by: 'event_type' %}
{% for group in e_grouped %}
  <h5>{{group.name}}</h5>  
  <ul>
  {% for e in group.items %}
    <li>
      <a href="{{ e.url }}">
        [{{ e.event_start | date: "%a, %d %B %Y" }}] {{ e.title }}
      </a>
    </li>
  {% endfor %}
  </ul>
{% endfor %}
