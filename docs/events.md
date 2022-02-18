---
title: Resources
layout: default
permalink: /events
---


{% assign e_all = site.event | sort: "start_date" | reverse %}
{% if e_all.size > 0 %}
  {% include event_list.html title="Events" events=e_all %}
{% endif %}


{% include event_slides.html %}