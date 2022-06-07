---
layout: default
---

<content>
{{ content }}

    <hr>

	<h2>Blog</h2>

	<ol reversed>
		{% for note in site.notes reversed %}
		{% if note.type == 'blog' %}
			<li><a href="{{ note.url }}">{{ note.title }}</a>  ({{ note.date | date_to_long_string: "ordinal" }})</li>
		{% endif %}
		{% endfor %}
	</ol>

<div class="grid-main-sidebar">

	<aside id="backlink-wrapper">
		<div id="backlink-content" class="sticky">
		<!-- Backlinks to go here -->
		</div>
	</aside>

	<div>

    {% for note in site.notes reversed %}
		{% if note.type == "blog" %}
			{% include blog-post.html %}
		{% endif %}
    {% endfor %}
	
	</div>
	
	</div>
</content>
