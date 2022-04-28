---
layout: page
title: default
id: home
permalink: /
---

# Mad Spinning Top

<h2>People</h2>

{% include people.html %}

<hr />

{% include notes_graph.html %}

<hr />
{% for note in site.notes reversed %}
{% if note.type == "blog" %}
{% include blog-post.html %}
{% endif %}
{% endfor %}
