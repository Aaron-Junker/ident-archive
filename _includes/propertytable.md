<script>
    function openAsPopup(url){
        var dialog = document.getElementById('helpdialog');
        var iframe = document.getElementById('helpdialogiframe');
        iframe.src = url + "?hideHeader";
        dialog.showModal();
        dialog.style.display = "block";

    }
function closePropertyDialog(id) {
    var dialog = document.getElementById(id);
    dialog.style.display = "none";
    dialog.close();
}
</script>
<dialog id="helpdialog" style="display:none; width: 90%;">
    <iframe width="100%" onload="resizeIframe(this)" height="100%" id="helpdialogiframe"></iframe>
    <button onClick="closePropertyDialog('helpdialog')">Close</button>
</dialog>
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