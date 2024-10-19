{% assign page_info = site.pages | find: 'smallname', include.language %}
{{ page_info.fullname }}test