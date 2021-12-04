---
title: Resources
layout: default
permalink: /events
---


{% assign e_future = site.event | where_exp: "item", "item.event_start > site.time" | sort: "start_date" | reverse %}
{% assign e_past = site.event | where_exp: "item", "item.event_start <= site.time" | sort: "start_date" | reverse %}
{% if e_future.size > 0 %}
  {% include event_list.html title="Upcoming Events" events=e_future %}
{% endif %}
{% if e_past.size > 0 %}
  {% include event_list.html title="Past Events" events=e_past %}
{% endif %}



{% include event_slides.html %}