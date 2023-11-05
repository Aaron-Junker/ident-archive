{% assign page_name = include.organization | append: '.md' %}
{% assign page_info = site.pages | where: 'name', page_name %}
{{ page_info[0].fullname }}