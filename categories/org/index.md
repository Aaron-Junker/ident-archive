---
layout: default
---
# Organizations

{% assign organizations = '' | split: '' %}
{% for p in site.entries %}
    {% unless organizations contains p.organization %}
        {% assign organizations = organizations | push: p.organization %}
    {% endunless %}
{% endfor %}
{% assign organizations = organizations | sort_natural %}
<ul>
{% for org in organizations %}
<li><a href="{{ org }}">{{ org }}</a></li>
{% endfor %}
</ul>