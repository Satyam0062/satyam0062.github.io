---

layout: archive
permalink: /projects/
title: "Projects"
author_profile: true
header:
  image: "/images/projects.jpg"
---

{% include skip-links.html %}
{% include group-by-array collection = site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[for loop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
