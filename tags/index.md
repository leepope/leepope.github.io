---
layout: default
title:  Tags
---

<h1>{{ page.title }}</h1>

{% capture tags %}
  {% for tag in site.tags %}
    {{ tag | first }}
  {% endfor %}
{% endcapture %}
{% assign sorted_tags = tags | split:' ' | sort %}
{% for tag in sorted_tags %}
  <h3 id="{{ tag  }}">{{ tag }}</h3>
  <ul>
  {% for post in site.tags[tag] %}
    <li>
      {% include post_list_item.html %}
    </li>
  {% endfor %}
  </ul>
{% endfor %}
