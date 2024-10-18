<script>
    function openAsPopup(url){
        window.open(url + "?hideHeader", "More Information", "scrollbars=no,resizable=no,status=no,location=no,toolbar=no, menubar=no,width=0,height=0,left=-1000,top=-300")
    }
</script>
<table>
    <thead>
        <tr>
            <th><b>Property:</b></th>
            <th><b>Value:</b></th>
        </tr>
    </thead>
    <tr>
        <td>Organization<a href="javascript:openAsPopup('/about/Properties/organization')">？</a></td>
        {% assign o=include.page.organization %}
        <td><a title="{% include fullorgname.md organization=o %}" href="/categories/org/{{ include.page.organization }}">{{ include.page.organization }}</a></td>
    </tr>
    <tr>
        <td>Title</td>
        <td>{{ include.page.title }}</td>
    </tr>
    <tr>
        <td>Watermark<a href="javascript:openAsPopup('/about/Properties/watermark')">？</a></td>
        <td>{{ include.page.watermark }}</td>
    </tr>
    <tr>
        <td>Language</td>
        {% assign l=include.page.language %}
        <td><a href="/categories/language/{{ include.page.language }}">{% include fulllanguagename.md language=l %}</a></td>
    </tr>
    <tr>
        <td>Date<a href="javascript:openAsPopup('/about/Properties/date')">？</a></td>
        <td>{{ include.page.usagedate }}</td>
    </tr>
    <tr>
        <td>Source<a href="javascript:openAsPopup('/about/Properties/source')">？</a></td>
        <td>{% if include.page.source %}<a href="{{include.page.sourceurl}}">{{ include.page.source }}</a>{% else %}<i>No information</i>{% endif %}</td>
    </tr>
</table>