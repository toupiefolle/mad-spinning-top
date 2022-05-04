---
layout: home
title: People
permalink: /people
---

<h1>{{ page.title }}</h1>

<ul>
    {% for note in site.notes %}
    {% if note.type == 'person' %}
    <li class="bold">{{ note.title }}</li>
		<ul>
		{% for backlink in note.backlinks %}
			<li><a href="{{ backlink.url }}">{{ backlink.title }}</a> ({{ backlink.date | date_to_long_string: "ordinal" }})</li>
		{% endfor %}
		</ul>
    {% endif %}
    {% endfor %}
</ul>

{% include notes_graph.html %}
