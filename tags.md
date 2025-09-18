---
layout: default
title: Tags
---

# Tags

<ul>
{% assign tags = site.tags | sort_natural %}
{% for tag in tags %}
  {% assign name = tag[0] %}
  <li><a href="{{ '/tag/' | append: name | relative_url }}/">#{{ name }}</a> ({{ tag[1].size }})</li>
{% endfor %}
</ul>

> Tip: To add a new tag page, copy `tag/intro.md` and change the `tag:` value.
