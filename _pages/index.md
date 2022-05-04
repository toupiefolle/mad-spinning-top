---
layout: home
title: default
id: home
permalink: /
---

# Mad Spinning Top

<h2>What's this all about?</h2>

See our [about page]({% link _pages/about.md %})

<hr />

<h2 class="blogroll">Blog</h2>

{% include blog-toc.html %}

{% for note in site.notes reversed %}
{% if note.type == "blog" %}
{% include blog-post.html %}
{% endif %}
{% endfor %}
