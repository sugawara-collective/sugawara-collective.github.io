---
layout: page
permalink: /works
title: Works
scripts: [/assets/js/tabs.js]
exclude: true
---

# SFW Fan Works

<div id="tabs-with-content">
	<div class="tabs">
	  <ul>
	    <li class="is-active"><a>Fics</a></li>
	    <li><a>Art</a></li>
	    <li><a>Other</a></li>
	  </ul>
	</div>
	<div>
    <section class="tab-content">
    	<div class="buttons filters">
    		<span class="filter-label">Filters: </span>
			<span class="button active is-smaller">All</span>
			<span class="button is-smaller">OTP</span>
			<span class="button is-smaller">Multiship</span>
			<span class="button is-smaller">Romantic</span>
			<span class="button is-smaller">Platonic</span>
		</div>
		{% for work in site.data.sfw %}
		<div class="written-work">
			<span class="credit">by: <strong>{{ work.author }}</strong> | {{ work.date }}</span>
			<a href="{{work.url}}"><h3>{{ work.title }}</h3></a>
			<div class="tags">
				{% for tag in work.tags %}
				<span class="tag">{{tag}}</span>
				{% endfor %}
			</div>
			<p class="summary">{{ work.summary }}</p>
		</div>
		{% endfor %}
   </section>
    <section class="tab-content">
      Section 2
    </section>
    <section class="tab-content">
      Section 3
    </section>
  </div>
</div>