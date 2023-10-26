---
title: "Wan Lab - News"
layout: textlay
excerpt: "News"
sitemap: false
permalink: /news/
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br>
  <em>{{ article.headline | markdownify}}</em></p>
{% endfor %}