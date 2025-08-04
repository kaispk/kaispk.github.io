---
layout: page
title: Publications
permalink: /publications/
---

# Publications

## Books

{% for pub in site.data.publications %}
{% if pub.type == "book" %}
**{{ pub.title }}** ({{ pub.year }})  
{{ pub.authors }}  
*{{ pub.publisher }}*
{% if pub.url and pub.url != "#" %}[[Link]]({{ pub.url }}){% endif %}
{% if pub.note %}*{{ pub.note }}*{% endif %}

{% endif %}
{% endfor %}

## Peer-Reviewed Articles

{% for pub in site.data.publications %}
{% if pub.tags contains "peer-reviewed" %}
**{{ pub.title }}** ({{ pub.year }})  
{{ pub.authors }}  
*{{ pub.journal }}*
{% if pub.url and pub.url != "#" %}[[Link]]({{ pub.url }}){% endif %}
{% if pub.note %}*{{ pub.note }}*{% endif %}

{% endif %}
{% endfor %}

## Encyclopedia Entries & Reference Works

{% for pub in site.data.publications %}
{% if pub.type == "encyclopedia" %}
**{{ pub.title }}** ({{ pub.year }})  
{{ pub.authors }}  
*{{ pub.journal }}*
{% if pub.url and pub.url != "#" %}[[Link]]({{ pub.url }}){% endif %}

{% endif %}
{% endfor %}

---

## By Research Area

### Democratic Theory & Social Epistemology
{% for pub in site.data.publications %}
{% if pub.tags contains "democracy" or pub.tags contains "epistemic" %}
- {{ pub.title }} ({{ pub.year }})
{% endif %}
{% endfor %}

### Environmental Ethics
{% for pub in site.data.publications %}
{% if pub.tags contains "environment" %}
- {{ pub.title }} ({{ pub.year }})
{% endif %}
{% endfor %}

### Rationality & Decision Theory
{% for pub in site.data.publications %}
{% if pub.tags contains "rationality" %}
- {{ pub.title }} ({{ pub.year }})
{% endif %}
{% endfor %}

---

*For working papers and other materials, please contact me directly.*