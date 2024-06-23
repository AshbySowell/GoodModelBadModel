---
layout: default
title: Changelog Index
---

# Changelog

New features and updates to GoodModelBadModel.


{% for changelog in site.changelogs %}
  <h2><a href="{{ changelog.url }}">{{ changelog.date | date: "%B %d, %Y" }}</a></h2>
  <p>{{ changelog.excerpt }}</p>
{% endfor %}
