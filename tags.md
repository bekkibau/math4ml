---
layout: default
title: Tags
permalink: /tags/
use_katex: true

---
<p>
  {% assign all_tags = "" | split: "," %}
  {% for post in site.posts %}
    {% for tag in post.tags %}
      {% unless all_tags contains tag %}
        {% assign all_tags = all_tags | push: tag %}
      {% endunless %}
    {% endfor %}
  {% endfor %}
  {% assign sorted_tags = all_tags | sort %}
  {% for tag in sorted_tags %}
    <a href="#{{ tag | slugify }}">{{ tag }}</a>{% unless forloop.last %}{% endunless %}
  {% endfor %}
</p>

{% for tag in sorted_tags %}
### <a id="{{ tag | slugify }}"></a> {{ tag }}

<ul>
  {% assign posts_with_tag = site.posts | where_exp: "post", "post.tags contains tag" | sort: "title" %}
  {% for post in posts_with_tag %}
    <li class="tag-post-item">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="post-date-right">{{ post.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>

{% endfor %}