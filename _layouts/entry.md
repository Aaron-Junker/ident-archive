---
layout: default
---
<h2> {{ page.fulltitle }} </h2>

<h3> Video </h3>

<video src="../media/{{ page.organisation }}-{{ page.title }}-{{ page.watermark }}-{{ page.language }}-{{page.usagedate}}.mp4" controls style="width: 100%;"></video>

<h3> Properties </h3>

<table>
    <tr>
        <td>Property</td>
        <td>Value</td>
    </tr>
    <tr>
        <td>Organisation</td>
        <td>{{ page.organisation }}</td>
    </tr>
    <tr>
        <td>Title</td>
        <td>{{ page.title }}</td>
    </tr>
    <tr>
        <td>Watermark</td>
        <td>{{ page.watermark }}</td>
    </tr>
    <tr>
        <td>Language</td>
        <td>{{ page.language }}</td>
    </tr>
    <tr>
        <td>Date</td>
        <td>{{ page.usagedate }}</td>
    </tr>
    <tr>
        <td>Source</td>
        <td>{% if page.source And page.source != "" %}{{ page.source }}{% else %}<i>No information</i>{% endif %}</td>
    </tr>
</table>

{% assign content = content | strip_newlines %}
{% unless content == "" %}
<h3> Additional information </h3>
{{ content }}
{% endunless %}
