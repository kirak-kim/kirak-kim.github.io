---
permalink: /
title: "Kirak Kim"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I'm a Ph.D. student at [AIRIS Lab](https://airislab.kaist.ac.kr), KAIST, and currently a visiting researcher at CARTE, University of Toronto.
My research explores virtual environments, artificial intelligence, and spatial audio, with a recent focus on text-to-RIR generation for room impulse responses. I'm particularly interested in audio experiences in virtual spaces.

---

## Publications
{: #publications }

{% assign categories = "international,demos,domestic" | split: "," %}
{% assign category_titles = "International Conferences,Posters, Demos, and Workshop Papers,Domestic (Korean)" | split: "," %}

{% for i in (0..2) %}
{% assign cat = categories[i] %}
{% assign cat_title = category_titles[i] %}
{% assign cat_posts = site.publications | where: "category", cat | sort: "date" | reverse %}
{% if cat_posts.size > 0 %}
### {{ cat_title }}

{% for post in cat_posts %}
- {% if post.paperurl %}[**{{ post.title }}**]({{ post.paperurl }}){% else %}**{{ post.title }}**{% endif %}  
  {{ post.authors }} · *{{ post.venue }}*
{% endfor %}

{% endif %}
{% endfor %}

---

## Art Projects
{: #art-projects }

{% assign art = site.portfolio | sort: "date" | reverse %}
{% for post in art %}
- **{% if post.url %}[{{ post.title }}]({{ post.url }}){% else %}{{ post.title }}{% endif %}**{% if post.venue %} · {{ post.venue }}{% endif %}{% if post.role %} · *{{ post.role }}*{% endif %} <span style="color:#888; font-size:0.85em;">({{ post.date | date: "%b %Y" }})</span>
{% endfor %}
