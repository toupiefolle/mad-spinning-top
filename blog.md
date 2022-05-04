---
layout: home
title: blog
id: home
permalink: /blog
---

<h1 class="blogroll">Blog</h1>

{% include blog-toc.html %}

{% for note in site.notes reversed %}
{% if note.type == "blog" %}
{% include blog-post.html %}
{% endif %}
{% endfor %}
