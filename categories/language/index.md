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
<li><a href="{{ l }}">{{ l }}</a></li>
{% endfor %}
</ul>