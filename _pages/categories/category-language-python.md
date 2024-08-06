---
title: "Python"
layout: archive
permalink: category/python
author_profile: true
header:
  overlay_image: "/assets/header.jpg"
  overlay_filter: 0.3 # same as adding an opacity of 0.5 to a black background
sidebar:
  nav: "sidebar-menu"
---

{% assign posts = site.categories.python %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}