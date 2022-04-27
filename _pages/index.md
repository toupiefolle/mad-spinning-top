---
layout: page
title: default
id: home
permalink: /
---

# 'Like a Mad Spinning Top'

{% include notes_graph.html %}

{% for note in site.notes reversed %}
{% if note.type == "blog" %}
{% include blog-post.html %}
{% endif %}
{% endfor %}
