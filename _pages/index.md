---
layout: home
title: default
id: home
permalink: /
---

# Mad Spinning Top

<h2>What's this all about?</h2>

See our [about page]({% link _pages/about.md %})

<h2>People</h2>

{% include people.html %}

{% include notes_graph.html %}

<hr />

<h2 class="blogroll">Blog</h2>

{% for note in site.notes reversed %}
{% if note.type == "blog" %}
{% include blog-post.html %}
{% endif %}
{% endfor %}
