---
layout: default
---
<h1>{{page.fullname}}</h1>
{% assign entries = site.entries | where: 'organization',page.smallname %}
<p><b>Number of entries</b>: {{entries | size}}</p>
{%if page.language %}
    <p><b>Language:</b> <a href="/categories/language/{{page.language}}">{% include fulllanguagename.md language=page.language %}</a></p>
    {% include table.html entries=entries hide_org=true hide_language=true %}
{% else %}
    {% include table.html entries=entries hide_org=true %}
{% endif %}