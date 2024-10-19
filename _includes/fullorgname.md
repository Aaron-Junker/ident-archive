{% comment %}
This include file is used to get the full name of an organization from the organization's short name.
Parameters:
- organization: The short name of the organization
{% endcomment %}

{% assign page_info = site.pages | find: 'smallname', include.organization %}
{{ page_info.fullname }}