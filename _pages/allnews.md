---
title: "News"
layout: textlay
excerpt: "Wan Lab@UNMC"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p>{{ article.date }}</p> <br>
<p><em>{{ article.headline | markdownify}}</em></p>
{% endfor %}
