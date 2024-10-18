

{% assign page_name = include.language | append: '.md' %}
{% assign page_info = site.pages | find: 'name', page_name %}
{{ page_info.fullname }}