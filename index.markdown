---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Recipes
---

{% assign groups = site.recipes | group_by: "category" | sort: "name" %}

{% for group in groups %}
<h3>{{ group.name }}</h3>
<ul>
    {% for recipe in group.items %}
    <li>
        <a href="{{ recipe.url | relative_url }}">
        {{ recipe.title }}
        </a>
    </li>
    {%endfor%}
</ul>
{% endfor %}