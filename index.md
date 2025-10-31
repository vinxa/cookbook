---
layout: default
title: Home
---

# 🍳 Gabby’s Cookbook

A collection of recipes written in [CookLang](https://cooklang.org) :)

## Recipes
<div class="recipe-grid">
{% for recipe in site.recipes_generated %}
  <a class="recipe-tile" href="{{ recipe.url | relative_url }}">
    <div class="recipe-tile-inner">
      <h2>{{ recipe.title | replace: '_', ' ' }}</h2>
      {% if recipe.servings %}
        <p>👥 {{ recipe.servings }} servings</p>
      {% endif %}
    </div>
  </a>
{% endfor %}
</div>

<style>
.recipe-card {
  max-width: 700px;
  margin: 2rem auto;
  background: #fffdfa;
  border-radius: 16px;
  padding: 2rem;
  box-shadow: 0 4px 16px rgba(0,0,0,0.08);
  font-family: "Inter", "Segoe UI", sans-serif;
}
.recipe-section h2 {
  border-bottom: 2px solid #f0d497;
  padding-bottom: .25rem;
  margin-bottom: .5rem;
}
.home-link {
  color: #a67c00;
  text-decoration: none;
  &:hover { text-decoration: underline; }
}
.recipe-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
  margin-top: 1rem;
}
.recipe-tile-inner {
  background: #fffdfa;
  border-radius: 12px;
  padding: 1rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
  transition: transform .15s ease, box-shadow .15s ease;
  &:hover {
    transform: translateY(-3px);
    box-shadow: 0 4px 10px rgba(0,0,0,0.15);
  }
  h2 {
    margin: 0 0 .5rem;
    font-size: 1.2rem;
    color: #222;
  }
  p {
    margin: 0;
    color: #666;
  }
}


body {
  background: #fffaf3;
}
h1, h2 {
  color: #222;
}

</style>