---
title: Blogs
layout: page
permalink: /blogs/
---

<div class="blogs">
    {% for post in site.posts %}
        {% if post.categories contains 'blogs' %}
            {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
        <li>
        <!-- <span>{{ post.date | date_to_string }} &raquo;</span>
        <a href="{{ post.url }}">{{ post.title }}</a> -->
        <span class="post-meta">{{ post.date | date_to_string }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        </li>
        {% endif %}
    {% endfor %}
</div>
