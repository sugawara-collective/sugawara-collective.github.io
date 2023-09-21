---
layout: page
permalink: /projects
title: Projects
---

# Projects
Please explore the past and ongoing projects.

<!-- <div class="buttons filters">
	<span class="button active">All</span>
	<span class="button ">Completed</span>
	<span class="button ">Current</span>
	<span class="button ">Upcoming</span>
	<span class="button ">Multiship</span>
	<span class="button ">Zine</span>
</div> -->

<div class="projects-container columns">
	{% for project in site.data.projects %}
	<div class="project-container column is-one-third-desktop is-half-tablet">
		<a href="{{project.url}}">
		<div class="project-title">
			<h4>{{project.title}} | {{project.year}}</h4>
		</div>
		<div class="project-details">
			<img class="image is-fullwidth" src="{{ project.imageSrc | prepend: site.baseurl }}"/>
			<div class="overlay">
				<div class="tags">
					{% for tag in project.tags %}
					<span class="tag">{{tag}}</span>
					{% endfor %}
				</div>
			</div>
		</div></a>
	</div>
	{% endfor %}
</div>