---
layout:  page
title:   Examples
---

Please select library part to show examples for:

<ul>
  {% assign sorted_pages = site.pages | sort:"name" %}
  {% for node in sorted_pages %}
	{% if node.categories contains "examples" %}
	  <li class="sidebar-nav-item{% if page.url == node.url %} active{% endif %}">
		<a href="{{ node.url }}">{{ node.menu-title }}</a>
	  </li>
	{% endif %}
  {% endfor %}
</ul>
