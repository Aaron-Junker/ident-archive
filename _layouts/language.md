---
layout: default
---
<h1>{{page.fullname}}</h1>
{% assign entries = site.entries | where: 'language',page.smallname %}
<p><b>Number of entries:</b> {{entries | size}}</p>
{% include table.html entries=entries hide_language=true %}