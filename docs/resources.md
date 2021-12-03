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

<h5>Event Slides</h5>
  {% assign r = site.collections | where: 'label', 'resource' | first %}
 
  <ul>
     {% for file in r.files | where: 'resource_type', 'slide' %}
    <li>
      <a href="{{ file.url }}">
          {{ file.basename }}
      </a>
    </li>
  {% endfor %}