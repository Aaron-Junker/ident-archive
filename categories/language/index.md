---
layout: default
---
# Languages

{% capture languages %}{% for p in entries %}{{ p.language }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign languages_list = languages | split:',' | sort_natural %}

<ul>
{% for l in languages_list %}
<li>[{{ l }}]({{ l | downcase | replace: ' ', '-' }})</li>
{% endfor %}
</ul>