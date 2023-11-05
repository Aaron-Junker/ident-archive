---
layout: default
---
<h1>{{page.fullname}}</h1>
<ul>
    {% for entry in site.entries %}
        {% if entry.organization == page.smallname %}
            <li><p><a href="{{entry.url}}">{{entry.fulltitle}}</a></p></li>
        {% endif %}
    {% endfor %}
</ul>