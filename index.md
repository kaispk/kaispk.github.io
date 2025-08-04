---
layout: home
title: Home
---

# Kai Spiekermann

I'm a Professor of Political Philosophy in the Department of Government at the London School of Economics. I work in democratic theory, the philosophy of the social sciences and topics relating to politics, philosophy and economics (PPE) more generally. 

Among my research interests are group decisions, social epistemology (and especially epistemic justifications of democracy), the ethics of environmental change, and the methodology of political theory and political science.

## Contact

**Email:** [k.spiekermann@lse.ac.uk](mailto:k.spiekermann@lse.ac.uk)

**Office hours:** Please book on the LSE Student Hub app.

## News

{% for item in site.data.news limit:5 %}
**{% if item.date %}{{ item.date }} - {% endif %}{{ item.title }}**  
{{ item.content }}
{% if item.url %}[Read more]({{ item.url }}){% endif %}

{% endfor %}

[View all news →](/news/)

## Featured Publication

{% for pub in site.data.publications %}
{% if pub.featured %}
**{{ pub.title }}** ({{ pub.year }})  
{{ pub.authors }}  
*{{ pub.publisher }}*  
[More information]({{ pub.url }})
{% break %}
{% endif %}
{% endfor %}

## Research Areas

- **Democratic Theory** - Epistemic justifications of democracy, group decision-making
- **Social Epistemology** - Collective knowledge and belief formation  
- **Environmental Ethics** - Ethics of climate change and environmental policy
- **Philosophy of Social Science** - Methodology in political theory and political science
- **Politics, Philosophy & Economics** - Interdisciplinary approaches to social problems