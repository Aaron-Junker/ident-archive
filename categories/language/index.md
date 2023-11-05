---
layout: default
---
# Languages

{% assign languages = '' | split: '' %}
{% for p in site.entries %}
    {% unless languages contains p.language %}
        {% assign languages = languages | push: p.language %}
    {% endunless %}
{% endfor %}
{% assign languages = languages | sort_natural %}
<ul>
{% for l in languages %}
{% assign page_name = l | append: '.md'%}
{% assign page_info = site.pages | where: 'name', page_name %}
<li><a href="{{ l }}">{{ page_info[0].fullname }}</a></li>
{% endfor %}
</ul>