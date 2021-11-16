---
title: Resources
layout: default
permalink: /resources
---

<h5>Documents</h5>

{% for r in site.resource %}  
  <a href="{{ r.url }}">
    {{ r.title }}
  </a>
{% endfor %}
