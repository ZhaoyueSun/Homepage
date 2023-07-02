---
title: Blogs
layout: page
# permalink: /homepage/blogs/
---

<div class="blogs">
    {% for post in site.posts %}
        {% if post.categories contains 'blogs' %}
            {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
        <li><span>{{ post.date | date_to_string }} &raquo;</span><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endif %}
    {% endfor %}
</div>
