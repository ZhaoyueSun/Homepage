---
title: Blogs
layout: page
permalink: /blog/
---

{% for post in site.posts %}
    {% if post.categories contains 'blog' %}
        {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
    <li><span>{{ post.date | date_to_string }} &raquo;</span><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
{% endfor %}