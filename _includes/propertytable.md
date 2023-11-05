<table>
    <thead>
        <tr>
            <td><b>Property:</b></td>
            <td><b>Value:</b></td>
        </tr>
    </thead>
    <tr>
        <td>Organization</td>
        {% assign o=include.page.organization %}
        <td><a title="{% include fullorgname.md organization=o %}" href="/categories/org/{{ include.page.organization }}">{{ include.page.organization }}</a></td>
    </tr>
    <tr>
        <td>Title</td>
        <td>{{ include.page.title }}</td>
    </tr>
    <tr>
        <td>Watermark</td>
        <td>{{ include.page.watermark }}</td>
    </tr>
    <tr>
        <td>Language</td>
        {% assign l=include.page.language %}
        <td><a href="/categories/language/{{ include.page.language }}">{% include fulllanguagename.md language=l %}</a></td>
    </tr>
    <tr>
        <td>Date</td>
        <td>{{ include.page.usagedate }}</td>
    </tr>
    <tr>
        <td>Source</td>
        <td>{% if include.page.source %}<a href="{{include.page.sourceurl}}">{{ include.page.source }}</a>{% else %}<i>No information</i>{% endif %}</td>
    </tr>
</table>