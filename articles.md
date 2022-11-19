---
title: Articles
layout: default
show_in_navigation: true
navigation_order: 2
lang: en
---

{% for article in site.pages | where: "lang", "en" %}{% unless article.ifsh == "sh" %}{% if article.url contains "done" %}✅ {% endif %}
[{{ article.title }}]({{ article.url }}), *{{ article.authors }}*, {{ article.date }}
{% endunless %}{% endfor %}
