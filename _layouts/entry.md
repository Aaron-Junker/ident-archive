---
layout: default
---
{% assign page_name = page.language | append: '.md' %}
{% assign page_info = site.pages | where: 'name', page_name %}
{% assign full_language_name = page_info[0].fullname %}

{% assign page_name = page.organization | append: '.md' %}
{% assign page_info = site.pages | where: 'name', page_name %}
{% assign full_org_name = page_info[0].fullname %}

<h2> Video </h2>

<video src="../media/{{ page.organization }}-{{ page.title }}-{{ page.watermark }}-{{ page.language }}-{{page.usagedate}}.mp4" controls style="width: 100%;"></video>

<h2> Properties </h2>

<table>
    <thead>
        <tr>
            <td><b>Property:</b></td>
            <td><b>Value:</b></td>
        </tr>
    </thead>
    <tr>
        <td>Organization</td>
        <td><a title="{{ full_org_name }}" href="/categories/org/{{ page.organization }}">{{ page.organization }}</a></td>
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
        <td><a href="/categories/language/{{ page.language }}">{{ full_language_name }}</a></td>
    </tr>
    <tr>
        <td>Date</td>
        <td>{{ page.usagedate }}</td>
    </tr>
    <tr>
        <td>Source</td>
        <td>{% if page.source %}<a href="{{page.sourceurl}}">{{ page.source }}</a>{% else %}<i>No information</i>{% endif %}</td>
    </tr>
</table>

{% assign content = content | strip_newlines %}
{% unless content == "" %}
<h2> Additional information </h2>
{{ content }}
{% endunless %}
