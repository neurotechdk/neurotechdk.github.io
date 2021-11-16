---
title: Resources
layout: default
permalink: /resources
---

<h5>Documents</h5>

{% for resource in site.resources %}  
  <a href="{{ resource.url }}">
    {{ resource.title }}
  </a>
{% endfor %}
