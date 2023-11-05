---
layout: default
---
<h1>{{page.fullname}}</h1>
{% assign entries = site.entries | where: 'language',page.smallname %}
{% include table.html entries=entries hide_language=true %}