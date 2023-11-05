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
{% assign page_name = org | append: '.md'%}
{% assign page_info = site.pages | where: 'name', page_name %}
<li><a href="{{ org }}">{{ page_info[0].fullname }}{% if page_info[0].fullname != page_info[0].smallname %} ({{page_info[0].smallname}}){%endif %}</a></li>
{% endfor %}
</ul>