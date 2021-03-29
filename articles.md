---
title: Articles
call_to_action: 
background_image_path:
large_header: false
show_in_navigation: true
navigation_order: 2
lang: en
---

{% for article in site.pages %}{% unless article.ifsh == "sh" %}
[{{ article.title }}]({{ article.url }}), *{{ article.authors }}*, {{ article.date }}
{% endunless %}{% endfor %}
