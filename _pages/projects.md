---

layout: archive
permalink: /projects/
title: "Projects"
author_profile: true
header:
  image: "/images/projects.jpg"
---
{% include group-by-array collection = site.posts field="tags" %}

  {% for post in site.posts %}
      {% include archive-single.html %}
