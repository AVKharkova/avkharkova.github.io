---
layout: home
title: "Портфолио"
---

# Мои проекты

<ul style="list-style:none; padding:0;">
  {% assign sorted_projects = site.projects | sort: 'order' %}
  {% for project in sorted_projects %}
    <li style="margin-bottom: 2.5em; border-radius:14px; background: #f7f7fb; padding: 16px 20px;">
      {% if project.cover %}
        <img src="{{ project.cover }}" alt="{{ project.title }}" style="width:100%; max-width:760px; border-radius:10px; margin-bottom:16px;">
      {% endif %}
      <h2 style="margin-bottom:4px;">{{ project.title }}</h2>
      <div style="color:#888; margin-bottom:7px;">{{ project.stack }}</div>
      {{ project.content | markdownify }}
      {% if project.github %}
        <a href="{{ project.github }}" target="_blank" style="color:#FDC500;">Посмотреть на GitHub</a>
      {% endif %}
    </li>
  {% endfor %}
</ul>
