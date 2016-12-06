---
layout: page
title: Tag Cloud
---

{% assign tags = site.tags | sort %}

{% for tag in tags %}
    <span class="site-tag">
        <a href="/tag-cloud.html#{{ tag | first | slugify }}" 
        style="font-size: {{ tag | last | size  |  times: 4 | plus: 80  }}%">
            {{ tag | first }} ({{ tag | last | size }})
        </a>
    </span>
{% endfor %}


<div>
    {% for tag in tags %}
        <div>
            <h1><a id="{{ tag | first | slugify }}">Posts with tag {{tag[0]}}</a></h1>
            <div>
                {% for post in site.tags[tag | first] %}
                    <a href="{{ post.url }}">{{ post.title }}</a>
                {% endfor %}
            </div>
        </div>
    {% endfor %}
</div>

<h1>testje</h1>
<div>
    {% for tag in tags %}
        <div>
        {% for taggy in tag %}
            <div>
            {{ taggy }} <br/>
            </div>
        {% endfor %}
        </div>
    {% endfor %}
</div>