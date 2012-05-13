---
layout: page
title: Aaron Bonham
tagline: Do you know how hard it was to get that bear to the cabin?
---
{% include JB/setup %}

{% for post in site.posts limit:10 %}

<div class="post-content">
	{% if post.link %}
	<h1><a href="{{ post.link }}">{{ post.title }}</a>&nbsp;<a href="{{ post.url | remove :'.html' }}" title="Permanent link to ‘{{ post.title }}’" class="permalink infinitysymbol">&infin;</a></h1>
	{% else %}
	<h1><a href="{{ post.url | remove :'.html' }}">{{ post.title }}</a></h1>
	{% endif %}

	<div class="date"><span>{{ post.date | date_to_long_string }}</span></div>

	<div class="description">
		{{ post.content }}
	</div>
</div>

{% endfor %}