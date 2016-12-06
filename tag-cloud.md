---
layout: page
title: Tag Cloud
---

<div>
    {% assign tags = site.tags | sort %}
    {% for tag in tags %}
        <span class="site-tag">
            <a href="/tag-cloud.html#{{ tag | first | slugify }}" 
            style="font-size: {{ tag | last | size  |  times: 20 | plus: 80  }}%">
                {{ tag | first }} ({{ tag | last | size }})
            </a>
        </span>
    {% endfor %}
</div>

<div>
    {% for tag in tags %}
        <div>
            {% assign tagname = tag[0] %}
            <h2><a id="{{ tag | first | slugify }}" class="post-title">Posts with tag {{tagname}}</a></h2>
            <div>
                {% for post in site.tags[tagname] %}
                    <a href="{{ post.url }}">{{ post.title }}</a>
                {% endfor %}
            </div>
        </div>
    {% endfor %}
</div>