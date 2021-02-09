---
layout: page
title: Workshop Schedule
---

{% if site.carpentry == "crs" %}
  {% include crs/schedule.md %}
{% elsif site.carpentry == "swc" %}
  {% include swc/schedule.html %}
{% elsif site.carpentry == "dc" %}
  {% include dc/schedule.html %}
{% elsif site.carpentry == "lc" %}
  {% include lc/schedule.html %}
{% endif %}
