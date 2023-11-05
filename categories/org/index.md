---
layout: default
---
# Organizations

{% capture organizations %}{% for p in entries %}{{ p.organization }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign organizations_list = organizations | split:',' | sort_natural %}

<ul>
{% for org in organizations_list %}
<li>[{{ org }}]({{ org | downcase | replace: ' ', '-' }})</li>
{% endfor %}
</ul>