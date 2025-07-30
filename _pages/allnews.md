---
title: "News"
layout: textlay
excerpt: "Allan Lab at Leiden University."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p><strong>{{ article.date }}</strong> – {% if article.link %}
      <a href="{{ article.link }}" target="_blank">{{ article.headline }}</a>
    {% else %}
      {{ article.headline }}
    {% endif %}</p>
{% endfor %}
