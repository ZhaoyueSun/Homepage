---
title: Blogs
layout: page
permalink: /homepage/blogs/
---

<div class="blogs">
    {% for post in site.posts %}
        {% if post.categories contains 'blogs' %}
            {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
        <li>
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        </li>
        {% endif %}
    {% endfor %}
</div>
