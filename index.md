---
title: Pravapis·org
lang: en
layout: default
---

The 2000s turned out to be the decade when the Belarusian Internet segment has known its fastest growth. Have appeared the platforms [Slounik·org](http://slounik.org) (Belarusian dictionaries), [Belarusian Bookshelf](https://knihi.com) (library) and the two Belarusian-language versions of Wikipedia: in [standard Belarusian](https://be.wikipedia.org/) and in its [reactionary recension](https://be-tarask.wikipedia.org/), among many others. One of the central  resources of this nascent Belarusian electronic landscape was the website *Pravapis·org* (Bel. ‘orthogrphy’) maintained by Uladzimir Katkoŭski in 2001 — 2005. The website gathered materials on Belarusan language, culture and other Belarus-related issues. In 2005, Uladzimir tragically perishes in a car accident; by that time the website contains about 70 articles in both Belarusan and English contributed by popularizers of the Belarusian culture from the metropolis and abroad. These accumulated materials are worth being conserved and trasmitted despite the instable technical situation of the domain and hosting of the original website (click <a href="https://pravapis.org" target="_blank">here</a> to see if it is still up). The team of the project [Belarusian Discourse](https://dyskurs.be) created this mirror. Its sources are hosted [on Github](https://github.com/dyskurs/pravapis.org).


## Authors
{% assign list = "" | split: ',' %}
{% for article in site.pages %}
{% for author in article.authors %}
{% unless list contains author %}{% assign list = list | push: author %}{% endunless %} 
{% endfor %}
{% endfor %}

{% for author in list | sort %} [{{author}}](/author/{{author}}) — {% endfor %}

{% for author in list %}
## {{author}}

{% for article in site.pages %}{% if article.authors contains author %}{% if article.url contains "done" %}✅ {% endif %}[{{article.title}}]({{article.url}}) *{{article.authors | join: ", "}}* <small style="color:grey">*{{article.date}}*</small>{% endif %}


{% endfor %}
{% endfor %}