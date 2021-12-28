---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Home
---

{% for recipe in site.recipes %}
  <h2>
    <a href="{{ recipe.url | relative_url }}">
      {{ recipe.title }}
    </a>
  </h2>
{% endfor %}