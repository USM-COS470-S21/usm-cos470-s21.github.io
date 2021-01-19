---
title: Assignments
permalink: /assignments
layout: default
---
# Assignments
----

<div class="projects">
	<ul class="post-list">
		{% assign assignments = site.assignments | where: "hidden", "false" | sort: 'order' %}
		{% for assignment in assignments %}
			<li>
				<h2><a class="post-link" href="{{ assignment.url | relative_url }}">{{ assignment.title | escape }}</a></h2>
				<span class="post-meta">{{ assignment.description | escape }}</span>
				{% assign date_format = site.minima.date_format | default: "%A, %B %-d, %Y at %I:%M%p" %}
			</li>
		{% endfor %}
	</ul>
</div>
