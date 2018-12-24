---
layout: archive
permalink: /projects/
title: "My work"
author_profile: true
header:
    image: ""
---
{% include base_path %}
{% inlcude group-by-array collection=site.posts field="tags" %}
 
{% for tag in group_names %}
 {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in post %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
  