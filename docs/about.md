---
title: About
layout: default
lastmod: '2021-11-15T17:22:56.577Z'
permalink: /about
---

### The Team
<div class="row row-cols-1 row-cols-sm-3 row-cols-md-4 g-4">
{% for person in site.profile %}
<div class="col">
  <div class="card h-100 box-shadow">
    <img class="card-img-top" src="{{ person.profile_image }}" alt="{{ person.title }}">
    <div class="card-body">
      <p class="card-text">{{ person.content }}</p>
      <div class="d-flex justify-content-between align-items-center">
        <div class="btn-group">
          <a href="{{ person.url }}" class="btn btn-sm btn-outline-secondary">Profile Page</a>
        </div>
      </div>
    </div>
    <div class="card-footer">
      <div class="d-flex justify-content-between w-75">
        {% include social_links_unwrapped.html person=person %}
      </div>
    </div>
  </div>
</div>
{% endfor %}
</div>

