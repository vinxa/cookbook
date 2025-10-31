---
layout: default
title: Home
---

# 🍳 Gabby’s Cookbook

A collection of recipes written in [CookLang](https://cooklang.org)! :)

## Recipes
<ul>
{% for recipe in site.recipes %}
  <li><a href="{{ recipe.url | relative_url }}">{{ recipe.title }}</a></li>
{% endfor %}
</ul>