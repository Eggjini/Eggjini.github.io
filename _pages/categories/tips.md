---
layout: archive
permalink: tips
title: "Tips"

author_profile: true
sidebar:
  nav: "docs"
---

{% assign posts = site.categories.tips %}
{% for post in posts %}
  {% include custom-archive-single.html type=entries_layout %}
{% endfor %}
