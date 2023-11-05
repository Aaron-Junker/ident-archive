{% assign page_name = include.language | append: '.md' %}
{% assign page_info = site.pages | where: 'name', page_name %}
{{ page_info[0].fullname }}