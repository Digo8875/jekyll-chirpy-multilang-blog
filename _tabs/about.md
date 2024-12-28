---
icon: fas fa-info-circle
order: 4
---

<!-- The file type (.md or .html) of about-content -->
{% assign file_type = '.md' %}

{% assign path_prefix = '' %}
{% assign file_name = 'about-content' %}

{% if site.active_lang == site.default_lang %}
  {% assign path_prefix = '' %}
{% else %}
  {% assign path_prefix = '' | append: site.active_lang | append: '/' %}
{% endif %}

{% assign about_content_path = '' | append: path_prefix | append: file_name | append: file_type %}

{% include {{ about_content_path }} %}
