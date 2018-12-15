---
excerpt: "Archived posts by category and date."
categories: archive, site, admin
layout: page
title: Archive
permalink: /archive/
created:
legacy-date:
---

<p><strong>Posts in a given category can be reached at:</strong></p>
<p><i>/category/[name of category]</i></p>
<p><strong>Posts in a given date range can be reach at:</strong></p>
<p><i>/archives/[year]</i><br>
<i>/archives/[year]/[month]</i><br>
<i>/archives/[year]/[month]/[day]</i></p>

<section id="category-list" class="piped-list">
<p><strong>Post categories with corresponding number of posts:</strong></p>
<ul>
	{% assign categories = site.categories | sort %}
	{% for category in site.categories %}
	<li>
		<a href="/category/{{ category | first | slugify }}/">{{ category[0] | replace:'-', ' ' }} ({{ category | last | size }})</a>
	</li>
	{% endfor %}
</ul>
</section>

<section id="date-list" class="piped-list">
<p><strong>Posts by year with corresponding number of posts:</strong></p>
<ul>
{% assign counter = 0 %}
{% for post in site.posts %}
  {% if post.date %}
    {% assign thisyear = post.date | date: "%Y" %}
    {% assign prevyear = post.previous.date | date: "%Y" %}
  {% endif %}
  {% assign counter = counter | plus: 1 %}
  {% if thisyear != prevyear %}
    <li><a href="/archives/{{ post.date | date:'%Y' }}">{{ thisyear }} ({{ counter }})</a></li>
    {% assign counter = 0 %}
  {% endif %}
{% endfor %}
</ul>
</section>
