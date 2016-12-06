---
layout: page
title: Tag Cloud
---

<div class="tag-cloud">
    {% assign tags = site.tags | sort %}
    {% for tag in tags %}
        <span class="site-tag">
            <a href="/tag-cloud.html#{{ tag | first | slugify }}" 
            style="font-size: {{ tag | last | size | times: 40 | plus: 60 }}%">
                {{ tag | first }} ({{ tag | last | size }})
            </a>
        </span>
    {% endfor %}
</div>

<div>
    {% for tag in tags %}
        <div class="tag-cloud-tag-div">
            {% assign tagname = tag[0] %}
            <h3><a id="{{ tag | first | slugify }}" class="tag-cloud-anchor">#{{tagname}}</a></h3>
            <div>
                {% for post in site.tags[tagname] %}
                    <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a><br/>
                {% endfor %}
            </div>
        </div>
    {% endfor %}
</div>