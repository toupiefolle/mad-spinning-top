---
layout: default
---

<content>
    {{ content }}

    <hr>

	<h2>Blog</h2>

    {% include blog-toc.html %}

    <hr>

    {% for note in site.notes reversed %}
    {% if note.type == "blog" %}
    {% include blog-post.html %}
    {% endif %}
    {% endfor %}
</content>
