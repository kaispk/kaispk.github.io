---
layout: single-no-sidebar
title: "Teaching"
permalink: /teaching/
author_profile: false
---

I teach courses in political philosophy, democratic theory, and research methods at the undergraduate and graduate levels. My teaching emphasizes critical thinking, rigorous argumentation, and the integration of theoretical and empirical approaches.

## Current Courses

**Democratic Theory**  
*Graduate seminar • Department of Government • LSE*

Advanced seminar examining contemporary debates in democratic theory, with special focus on epistemic approaches to democracy, deliberative democracy, and the challenge of political disagreement.

**Political Philosophy**  
*Undergraduate course • Department of Government • LSE*

Introduction to major themes in political philosophy including justice, liberty, equality, democracy, and political obligation. Covers both classical and contemporary approaches.

**Philosophy of Social Science**  
*Graduate course • Department of Government • LSE*

Methodological foundations of social science research, including the role of formal methods, causal inference, and the relationship between normative and empirical theory.

## Teaching Philosophy

My teaching emphasizes:

- **Critical engagement** with primary texts and contemporary debates
- **Rigorous argumentation** and clear philosophical writing
- **Interdisciplinary approaches** connecting philosophy with social science
- **Application** of theoretical insights to real-world problems
- **Student participation** through discussion, presentations, and collaborative work

## Supervision

I regularly supervise:

- **PhD dissertations** in political philosophy and democratic theory
- **MSc dissertations** in political theory and public policy
- **Undergraduate dissertations** in government and philosophy

For PhD supervision information, see my [supervision guidelines](/phd-supervision/).

## Office Hours

**Office hours:** Please book on the LSE Student Hub app

I maintain regular office hours for student consultations and am available for academic advising on research projects, career planning, and graduate school applications.

## Additional Teaching

{% for post in site.teaching reversed %}
**{{ post.title }}**  
{% if post.type %}*{{ post.type }}*{% endif %}{% if post.venue %}{% if post.type %} • {% endif %}*{{ post.venue }}*{% endif %}{% if post.date %} • {{ post.date | date: "%Y" }}{% endif %}

{% if post.excerpt %}{{ post.excerpt }}{% endif %}

{% if post.paperurl or post.slidesurl %}
{% if post.paperurl %}[Course Materials]({{ post.paperurl }}) {% endif %}
{% if post.slidesurl %}[Slides]({{ post.slidesurl }}){% endif %}
{% endif %}

{% endfor %}