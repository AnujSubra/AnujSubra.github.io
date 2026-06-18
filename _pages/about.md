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

<p>{{ author.summary }}</p>

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

## About me
<p>I am based in {{ author.location }} and I build research-driven projects in machine learning, physics, and computational mechanics.</p>

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

<p>My full CV is available at <a href="/cv/">/cv/</a>. To update career and experience details, edit <code>_data/cv_input.yml</code>.</p>
