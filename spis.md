---
layout: page
title: Spis treści
permalink: /spis/
---

{% assign cats = site.categories | sort %}

{% for cat in cats %}
## {{ cat[0] | replace: "-", " " | capitalize }}

{% assign posts = cat[1] | sort: "date" | reverse %}
{% for post in posts %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

{% endfor %}