<table>
    <thead>
        <tr>
            <td><b>Name</b></td>
            {% unless include.hide_org %}
            <td><b>Organization</b></td>
            {% endunless %}
            {% unless include.hide_language %}
            <td><b>Language</b></td>
            {% endunless %}
            <td><b>Date</b></td>
            <td><b>Watermark</b></td>
        </tr>
    </thead>
    {% for entry in include.entries %}
    <tr>
        <td><a href="{{entry.url}}">{{entry.fulltitle}}</a></td>
        {% unless include.hide_org %}
        <td><a title="{% include fullorgname.md language=entry.organization %}" href="/categories/org/{{ entry.organization }}">{{ entry.organization }}</a></td>
        {% endunless %}
        {% unless include.hide_language %}
        <td><a href="/categories/language/{{ entry.language }}">{% include fullanguagename.md language=entry.language %}</a></td>
        {% endunless %}
        <td>{{ entry.usagedate }}</td>
        <td>{{ entry.watermark }}</td>
    </tr>
    {% endfor %}
</table>