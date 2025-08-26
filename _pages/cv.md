---
layout: single-no-sidebar
title: "Curriculum Vitae"
permalink: /cv/
author_profile: false
redirect_from:
  - /resume
---

{% include base_path %}

<style>
  .cv-section {
    margin-bottom: 30px;
  }
  
  .cv-section h2 {
    color: #2c3e50;
    border-bottom: 2px solid #3498db;
    padding-bottom: 8px;
    margin-bottom: 20px;
    font-size: 1.3em;
  }
  
  .cv-item {
    margin-bottom: 20px;
    font-size: 0.9em;
    line-height: 1.5;
  }
  
  .cv-item h3 {
    margin: 0 0 5px 0;
    font-size: 1em;
    font-weight: 600;
    color: #2c3e50;
  }
  
  .cv-item .details {
    color: #555;
    margin-bottom: 5px;
    font-size: 0.95em;
  }
  
  .cv-item .description {
    color: #666;
    font-size: 0.9em;
    line-height: 1.4;
  }
  
  .download-links {
    text-align: center;
    margin: 30px 0;
    padding: 20px;
    background: #f8f9fa;
    border-radius: 8px;
  }
  
  .download-links a {
    display: inline-block;
    padding: 10px 20px;
    margin: 0 10px;
    background: #3498db;
    color: white;
    text-decoration: none;
    border-radius: 5px;
    font-size: 0.9em;
  }
  
  .download-links a:hover {
    background: #2980b9;
  }
</style>

<div class="download-links">
  <a href="/files/cv.pdf">Download CV as PDF</a>
</div>

## Current Position

<div class="cv-section">
  <div class="cv-item">
    <h3>Professor of Political Philosophy</h3>
    <div class="details">Department of Government, London School of Economics • 2015-present</div>
    <div class="description">
      Research and teaching in democratic theory, philosophy of social sciences, and politics, philosophy and economics (PPE). 
      Current projects focus on epistemic democracy, environmental ethics, and collective decision-making.
    </div>
  </div>
</div>

## Education

<div class="cv-section">
  <div class="cv-item">
    <h3>Ph.D. in Philosophy</h3>
    <div class="details">University • Year</div>
    <div class="description">Dissertation: "Title of Dissertation"</div>
  </div>
  
  <div class="cv-item">
    <h3>M.A. in Philosophy</h3>
    <div class="details">University • Year</div>
  </div>
  
  <div class="cv-item">
    <h3>B.A. in Philosophy and Politics</h3>
    <div class="details">University • Year</div>
  </div>
</div>

## Previous Positions

<div class="cv-section">
  <div class="cv-item">
    <h3>Associate Professor</h3>
    <div class="details">Department of Government, London School of Economics • 2010-2015</div>
  </div>
  
  <div class="cv-item">
    <h3>Assistant Professor</h3>
    <div class="details">Department of Government, London School of Economics • 2005-2010</div>
  </div>
</div>

## Current Research Grants

<div class="cv-section">
  <div class="cv-item">
    <h3>Cohesive Capitalism Project</h3>
    <div class="details">Open Society Foundation • 2024-2027 • Co-investigator</div>
    <div class="description">
      Research on cohesion and deliberation in democratic decision-making, and protection against severe uncertainty.
      Collaboration with Alex Voorhoeve and Richard Bradley.
    </div>
  </div>
  
  <div class="cv-item">
    <h3>Augmenting Intelligence through Collective Learning</h3>
    <div class="details">NSF Research Coordination Network • 2024 • Research Associate</div>
    <div class="description">
      Examining how groups can enhance their collective intelligence through structured learning processes.
    </div>
  </div>
</div>

## Publications

### Books
<ul>
{% for post in site.publications reversed %}
  {% if post.category == "books" %}
    <li style="margin-bottom: 8px; font-size: 0.9em;">
      <strong>{{ post.title }}</strong> 
      {% if post.authors %}({{ post.authors }}){% endif %}
      {% if post.venue %}{{ post.venue }}{% endif %}
      {% if post.date %}{{ post.date | date: "%Y" }}{% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>

### Journal Articles
<ul>
{% for post in site.publications reversed %}
  {% if post.category == "manuscripts" %}
    <li style="margin-bottom: 8px; font-size: 0.9em;">
      <strong>{{ post.title }}</strong> 
      {% if post.authors %}({{ post.authors }}){% endif %}
      {% if post.venue %}<em>{{ post.venue }}</em>{% endif %}
      {% if post.date %}{{ post.date | date: "%Y" }}{% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>

### Encyclopedia Entries
<ul>
{% for post in site.publications reversed %}
  {% if post.category == "encyclopedia" %}
    <li style="margin-bottom: 8px; font-size: 0.9em;">
      <strong>{{ post.title }}</strong> 
      {% if post.authors %}({{ post.authors }}){% endif %}
      {% if post.venue %}<em>{{ post.venue }}</em>{% endif %}
      {% if post.date %}{{ post.date | date: "%Y" }}{% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>

## Editorial Service

<div class="cv-section">
  <div class="cv-item">
    <h3>Editorial Board Member</h3>
    <div class="details">Political Philosophy Journal • 2024-present</div>
  </div>
</div>

## Professional Service

<div class="cv-section">
  <div class="cv-item">
    <h3>Conference Organization</h3>
    <div class="details">Anne Phillips Fest (with Bruno Leipold) • 2024</div>
    <div class="description">Organized conference to mark the retirement of colleague Anne Phillips.</div>
  </div>
</div>

## Teaching

<div class="cv-section">
{% for post in site.teaching reversed %}
  <div class="cv-item">
    <h3>{{ post.title }}</h3>
    {% if post.type or post.venue or post.date %}
      <div class="details">
        {% if post.type %}{{ post.type }}{% endif %}
        {% if post.venue %}{% if post.type %} • {% endif %}{{ post.venue }}{% endif %}
        {% if post.date %} • {{ post.date | date: "%Y" }}{% endif %}
      </div>
    {% endif %}
    {% if post.excerpt %}
      <div class="description">{{ post.excerpt }}</div>
    {% endif %}
  </div>
{% endfor %}
</div>