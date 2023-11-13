<table>
    <thead>
        <tr>
            <th><b>Property:</b></th>
            <th><b>Value:</b></th>
        </tr>
    </thead>
    <tr>
        <td>Organization<a href="/about/Properties/Organization">？</a></td>
        {% assign o=include.page.organization %}
        <td><a title="{% include fullorgname.md organization=o %}" href="/categories/org/{{ include.page.organization }}">{{ include.page.organization }}</a></td>
    </tr>
    <tr>
        <td>Title</td>
        <td>{{ include.page.title }}</td>
    </tr>
    <tr>
        <td>Watermark<a href="/about/Properties/Watermark">？</a></td>
        <td>{{ include.page.watermark }}</td>
    </tr>
    <tr>
        <td>Language</td>
        {% assign l=include.page.language %}
        <td><a href="/categories/language/{{ include.page.language }}">{% include fulllanguagename.md language=l %}</a></td>
    </tr>
    <tr>
        <td>Date<a href="/about/Properties/Date">？</a></td>
        <td>{{ include.page.usagedate }}</td>
    </tr>
    <tr>
        <td>Source<a href="/about/Properties/Source">？</a></td>
        <td>{% if include.page.source %}<a href="{{include.page.sourceurl}}">{{ include.page.source }}</a>{% else %}<i>No information</i>{% endif %}</td>
    </tr>
</table>