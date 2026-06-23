---
permalink: /
title: "Kirak Kim"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

Hi! I'm a Ph.D. student at [AIRIS Lab](https://airislab.kaist.ac.kr), KAIST, and currently a visiting researcher at CARTE, University of Toronto.
My research explores virtual environments, artificial intelligence, and spatial audio, with a recent focus on text-to-RIR generation for room impulse responses. I'm particularly interested in audio experiences in virtual spaces.

---

## Publications
{: #publications }

### International Conferences

{% assign cat_posts = site.publications | where: "category", "international" | sort: "date" | reverse %}
{% for post in cat_posts %}
<div style="margin-bottom: 1.2em;">
  <div><strong>{{ post.title }}</strong>{% if post.paperurl %} <a href="{{ post.paperurl }}" target="_blank" rel="noopener noreferrer" style="font-size:0.85em;">[Link]</a>{% endif %}</div>
  <div style="font-size:0.85em; margin-top:0.15em;">{{ post.authors }}</div>
  <div style="font-size:0.85em; color:#888; margin-top:0.1em;">{{ post.venue }}</div>
</div>
{% endfor %}

### Posters, Demos, and Workshop Papers

{% assign cat_posts = site.publications | where: "category", "demos" | sort: "date" | reverse %}
{% for post in cat_posts %}
<div style="margin-bottom: 1.2em;">
  <div><strong>{{ post.title }}</strong>{% if post.paperurl %} <a href="{{ post.paperurl }}" target="_blank" rel="noopener noreferrer" style="font-size:0.85em;">[Link]</a>{% endif %}</div>
  <div style="font-size:0.85em; margin-top:0.15em;">{{ post.authors }}</div>
  <div style="font-size:0.85em; color:#888; margin-top:0.1em;">{{ post.venue }}</div>
</div>
{% endfor %}

### Domestic (Korean)

{% assign cat_posts = site.publications | where: "category", "domestic" | sort: "date" | reverse %}
{% for post in cat_posts %}
<div style="margin-bottom: 1.2em;">
  <div><strong>{{ post.title }}</strong>{% if post.paperurl %} <a href="{{ post.paperurl }}" target="_blank" rel="noopener noreferrer" style="font-size:0.85em;">[Link]</a>{% endif %}</div>
  <div style="font-size:0.85em; margin-top:0.15em;">{{ post.authors }}</div>
  <div style="font-size:0.85em; color:#888; margin-top:0.1em;">{{ post.venue }}</div>
</div>
{% endfor %}

---

## Art Projects
{: #art-projects }

{% assign art = site.portfolio | sort: "date" | reverse %}
{% for post in art %}
<div style="margin-bottom: 1.2em;">
  <div><strong>{% if post.external_url %}<a href="{{ post.external_url }}" target="_blank" rel="noopener noreferrer">{{ post.title }}</a>{% else %}{{ post.title }}{% endif %}</strong></div>
  {% if post.role and post.role != "" %}<div style="font-size:0.85em; margin-top:0.15em;">{{ post.role }}</div>{% endif %}
  <div style="font-size:0.85em; color:#888; margin-top:0.1em;">{% if post.venue and post.venue != "" %}{{ post.venue }} · {% endif %}{{ post.date | date: "%b %Y" }}</div>
</div>
{% endfor %}
