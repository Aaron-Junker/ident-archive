---
layout: default
---
<h1>{{page.fullname}}</h1>
{% assign entries = site.entries | where: 'organization',page.smallname %}

{% if page.suborgs %}
    <h2>Suborganisations</h2>
    <ul>
    {% assign suborgs = page.suborgs | split: ',' %}
    {% for suborg in suborgs %}
        <li><a href="/categories/org/{{suborg}}">{%include fullorgname.md organization=suborg %}</a></li>
    {% endfor %}
    </ul>
{% endif %}
<b style="display: inline;">Number of entries:</b> <p style="display: inline;" data-target="{{entries | size}}" class="counter">0</p><br><br>
{%if page.language %}
    <p><b>Language:</b> <a href="/categories/language/{{page.language}}">{% include fulllanguagename.md language=page.language %}</a></p>
    {% include table.html entries=entries hide_org=true hide_language=true %}
{% else %}
    {% include table.html entries=entries hide_org=true %}
{% endif %}