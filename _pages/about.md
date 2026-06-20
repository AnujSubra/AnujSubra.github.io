---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

{% assign author = site.data['portfolio-data'].author %}
{% assign portfolio_items = site.data['portfolio-data'].portfolio %}
{% assign publications = site.data['portfolio-data'].publications %}



## About me
<p>{{ author.summary }}</p>

### My interests and focus areas
<p>I'm drawn to problems that sit at the intersection of multiple disciplines. My current work spans:</p>
<ul>
  <li><strong>Machine Learning:</strong> Applying neural networks and data science to real-world challenges from music analysis to driver risk assessment and safety optimization.</li>
  <li><strong>Physics & Engineering:</strong> Modeling complex systems like aerodynamics and vehicle dynamics, with an emphasis on computational approaches and reduced-order modeling.</li>
  <li><strong>Civic Impact:</strong> Building technology solutions for community challenges, including the BG Safety Dashboard that maps traffic safety data to inform policy decisions.</li>
  <li><strong>Education & Accessibility:</strong> Supporting platforms and research that make learning opportunities more discoverable and accessible to others.</li>
</ul>

{% if portfolio_items and portfolio_items.size > 0 %}
## Featured work
<p>Current work includes:</p>
<ul>
{% for item in portfolio_items %}
  <li><strong><a href="{{ item.url }}">{{ item.name }}</a></strong> — {{ item.category }}{% if item.date %}, {{ item.date | date: "%Y" }}{% endif %}. {{ item.description }}</li>
{% endfor %}
</ul>
{% endif %}

{% if publications and publications.size > 0 %}
## Research highlights
<ul>
{% for pub in publications %}
  <li><a href="{{ pub.website }}">{{ pub.title }}</a> — {{ pub.publisher }}{% if pub.release_date %}, {{ pub.release_date | date: "%Y" }}{% endif %}</li>
{% endfor %}
</ul>
{% endif %}


### How I work
<p>I'm most energized when I can dive deep into rigorous coursework and research while building tangible projects. I'm comfortable picking up new tools and frameworks quickly, from audio production software to data platforms, and I enjoy collaborating with teams to transform ideas into impact.</p>

## Connect
<ul>
  {% if author.website %}<li>Website: <a href="{{ author.website }}">{{ author.website }}</a></li>{% endif %}
  {% if author.email %}<li>Email: <a href="mailto:{{ author.email }}">{{ author.email }}</a></li>{% endif %}
  {% if site.data['portfolio-data'].profiles %}
    {% for profile in site.data['portfolio-data'].profiles %}
      <li><a href="{{ profile.url }}">{{ profile.network }}</a></li>
    {% endfor %}
  {% endif %}
</ul>


