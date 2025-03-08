---
layout: default
---

# {{ page.title }}

This page automatically lists all pages tagged with **{{ page.title }}**.

{% for page in site.pages %}
  {% if page.tags contains page.title %}
  - [{{ page.title }}]({{ page.url }})
  {% endif %}
{% endfor %}
