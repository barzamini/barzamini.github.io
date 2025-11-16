---
layout: page
title: Publications
permalink: /publications/
---

# Publications

## Journals

{% assign journal_pubs = site.data.publications | where: "type", "journal" %}
{% for pub in journal_pubs %}
- **{{ pub.title }}**  
  {{ pub.authors }} ({{ pub.year }}). *{{ pub.venue }}*{% if pub.volume %}, {{ pub.volume }}{% endif %}{% if pub.pages %}, {{ pub.pages }}{% endif %}.  
  {% if pub.pdf %}[PDF]({{ pub.pdf | relative_url }}){% endif %}
{% endfor %}

## Conferences

{% assign conference_pubs = site.data.publications | where: "type", "conference" %}
{% for pub in conference_pubs %}
- **{{ pub.title }}**  
  {{ pub.authors }} ({{ pub.year }}). In *{{ pub.venue }}*{% if pub.pages %}, {{ pub.pages }}{% endif %}.  
  {% if pub.pdf %}[PDF]({{ pub.pdf | relative_url }}){% endif %}
{% endfor %}

