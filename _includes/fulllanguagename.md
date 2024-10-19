{% assign page_info = site.pages | find: 'smallname', include.language %}
{{ include.language }}:
{{ page_info }}
{{ page_info.fullname }}