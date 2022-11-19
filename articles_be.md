---
title: Артыкулы
call_to_action: 
background_image_path:
show_in_navigation: true
navigation_order: 2
lang: be
---

{% for article in site.pages | where: "lang", "be"  %}{% unless article.ifsh == "sh" %}
{% if article.url contains "done" %}✅ {% endif %} [{{ article.title }}]({{ article.url }}), *{{ article.authors }}*, {{ article.date }}

{% endunless %}{% endfor %}
