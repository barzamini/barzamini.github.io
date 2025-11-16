---
layout: page
title: News
permalink: /news/
---

# News

{% for item in site.data.news %}
- **{{ item.date | date: "%B %Y" }}**: {{ item.content }}
{% endfor %}

