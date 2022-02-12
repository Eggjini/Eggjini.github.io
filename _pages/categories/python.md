---
layout: archive
permalink: python
title: "파이썬"

author_profile: true
sidebar:
  nav: "docs"
---

{% assign posts = site.categories.python %}
{% for post in posts %}
  {% include custom-archive-single.html type=entries_layout %}
{% endfor %}
