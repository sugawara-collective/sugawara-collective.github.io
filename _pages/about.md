---
layout: page
permalink: /about
title: Members
exclude: true
---

# Collective Members
Please check out the members.

<div class="columns align-top">
	{% for member in site.data.members %}
    <div class="column is-one-fifth-desktop is-one-third-tablet  member-container" {% for category in member.filters %} {{ category | prepend: 'data-'}} {% endfor %} >
    	<a class="primary-link" href="{{member.url}}">
        <div class="member-photo">
          <figure class="image is-square">
            <img class="is-rounded" src="{{ member.photo }}">
          </figure>
        </div>
        <h3 class="name">{{ member.name }}</h3></a>
        <div class="buttons member-socials">
            {% for social in member.socials %}
            <a id="{{ social.type }}" class="link is-fullwidth has-icon is-link is-primary" href="{{ social.url}}" target="_blank">
              <span id="{{ social.type }}" class="icon"></span>
              <span>{{ social.handle }}</span>
            </a>
            {% endfor %}
        </div>
    </div>
    {% endfor %}
</div>