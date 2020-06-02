---
layout: timeline
title: Timeline
---

<div class="container row">
	<h2 class="cv-title"><span class="black white-text">{{ page.title }}</span></h2>
	{% assign steps = site.steps | sort: 'date' %}
	{% for step in steps %}
	<div class="item">
		<i class="vertical-line"></i>
		<h3 class="item-date">{{ step.date | date: '%m/%d/%Y' }}{% if step.enddate %} - {{ step.enddate | date: '%m/%d/%Y' }}{% endif %}</h3>
		<div class="card-panel">
			<h4 class="card-title">
				{{ step.title }}
			</h4>
			<p>
				{{ step.content }}
			</p>
		</div>
</div>
{% endfor %}
<div class="last-item">
<i class="vertical-line"></i>
