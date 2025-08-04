---
layout: default
---

# Kai Spiekermann

I'm a Professor of Political Philosophy in the Department of Government at the London School of Economics. I work in democratic theory, the philosophy of the social sciences and topics relating to politics, philosophy and economics (PPE) more generally. 

Among my research interests are group decisions, social epistemology (and especially epistemic justifications of democracy), the ethics of environmental change, and the methodology of political theory and political science.

## About My Work

My research sits at the intersection of political philosophy, epistemology, and social science methodology. I'm particularly interested in how groups make decisions and form beliefs, and what this means for democratic theory and practice.

Current projects include work on epistemic democracy, environmental ethics and intergenerational justice, and the methodology of political theory. I'm also involved in several collaborative research initiatives exploring collective decision-making and social epistemology.

## Featured Publication

{% for pub in site.data.publications %}
{% if pub.featured %}
<div class="publication">
**{{ pub.title }}** ({{ pub.year }})  
{{ pub.authors }}  
*{{ pub.publisher }}*  
[More information]({{ pub.url }})
</div>
{% break %}
{% endif %}
{% endfor %}

## Recent Publications

{% for pub in site.data.publications limit:3 %}
<div class="publication">
**{{ pub.title }}** ({{ pub.year }})  
{{ pub.authors }}  
{% if pub.journal %}*{{ pub.journal }}*{% endif %}
{% if pub.publisher %}*{{ pub.publisher }}*{% endif %}
{% if pub.url and pub.url != "#" %}[Link]({{ pub.url }}){% endif %}
{% if pub.note %}*{{ pub.note }}*{% endif %}
</div>
{% endfor %}

[View all publications →]({{ '/publications/' | relative_url }})

## Teaching & Supervision

I teach courses in political philosophy, democratic theory, and research methods. I'm always interested in supervising PhD students working in areas related to my research interests.

If you're considering applying for a PhD, please see my [supervision guidelines]({{ '/could-i-be-your-supervisor/' | relative_url }}) for detailed information about the application process and what I look for in potential students.