---
title: Projects
permalink: /projects
layout: default
---
# Project Assignments
----
<div class="projects">
	<ul class="post-list">
		{% assign projects = site.projects | where: "hidden", "false" | sort: 'order' %}
		{% for project in projects %}
			<li>
				<h2><a class="post-link" href="{{ project.url | relative_url }}">{{ project.title | escape }}</a></h2>
				<span class="post-meta">{{ project.description | escape }}</span>
				{% assign date_format = site.minima.date_format | default: "%A, %B %-d, %Y at %I:%M%p" %}
				Due: <span class="post-meta due-date">{{ project.due | date: date_format }}</span>
			</li>
		{% endfor %}
	</ul>
</div>

Start your project by using the _Start the Project_ link in [Blackboard](https://bb.courses.maine.edu). This will create a private [GitHub](https://github.com) repository that you will `clone` and do all your work in. Projects are submitted by being pushed to [GitHub](https://github.com) before their due date and time.