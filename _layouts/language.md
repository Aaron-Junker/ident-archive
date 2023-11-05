---
layout: default
---
<h1>{{page.fullname}}</h1>
<ul>
    {% for entry in site.entries %}
        {% if entry.language == page.smallname %}
            <li><a href="{{entry.url}}">{{entry.fulltitle}}</a></li>
        {% endif %}
    {% endfor %}
</ul>