{% comment %}
This include file is used to get the full name of an organization from the organization's short name.
Parameters:
- organization: The short name of the organization
{% endcomment %}

{% assign page_name = include.organization | append: '.md' %}
{% assign page_info = site.pages | where: 'name', page_name %}
{{ page_info[0].fullname }}