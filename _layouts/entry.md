---
layout: default
---
{% assign page_name = page.language | append: '.md' %}
{% assign page_info = site.pages | where: 'name', page_name %}
{% assign full_language_name = page_info[0].fullname %}

{% assign page_name = page.organization | append: '.md' %}
{% assign page_info = site.pages | where: 'name', page_name %}
{% assign full_org_name = page_info[0].fullname %}
<h1> {{ page.fulltitle }} </h1>
<h2> Video </h2>

{% capture fileExtension %}{% if page.fileExtension %}{{ page.fileExtension }}{% else %}mp4{% endif %}{% endcapture %}

<video src="../media/{{ page.organization }}-{{ page.title }}-{{ page.watermark }}-{{ page.language }}-{{page.usagedate}}.{{fileExtension}}" controls style="width: 100%;"></video>

<h2> Properties </h2>

{% include propertytable.md page=page %}

{% assign content = content | strip_newlines %}
{% unless content == "" %}
<h2> Additional information </h2>
{{ content }}
{% endunless %}
