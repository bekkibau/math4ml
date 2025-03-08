---
layout: default
title: Math4ML
---

This is my collection of notes on math for machine learning.  
Using **KaTeX’s own font** makes everything look much better.

Check that these equations **blend well with the text**:  

Inline: $E = mc^2$ looks smooth inside a sentence.

Block math:
$$
\int_0^\infty e^{-x^2} \,dx = \frac{\sqrt{\pi}}{2}
$$

## Tags
These are the tags:

{% assign all_tags = "" | split: "," %}
{% for page in site.pages %}
  {% for tag in page.tags %}
    {% unless all_tags contains tag %}
      {% assign all_tags = all_tags | push: tag %}
    {% endunless %}
  {% endfor %}
{% endfor %}

{% for tag in all_tags %}
- [{{ tag | capitalize }}](/tags/{{ tag }}/)
{% endfor %}