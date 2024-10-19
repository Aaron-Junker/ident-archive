---
layout: default
---
<h1>{{page.fullname}}</h1>
{% assign entries = site.entries | where: 'language',page.smallname %}
<b style="display: inline;">Number of entries:</b> <p style="display: inline;" data-target="{{entries | size}}" class="counter">0</p><br><br>
{% include table.html entries=entries hide_language=true %}