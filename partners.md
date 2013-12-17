---
layout: default
title: Social Data Science - Potential Partners
---
Potential Partners
--------------------------------

Relevant organizations, groups, and individuals:

<ul>
{% for p in site.pages %}
  {% if p.layout == 'partner' %}
  
    <li class="partner-item">
  
      <span class="partner-name">
        {% if p.is-full-page %}
          <a href="{{ p.url }}">{{ p.partner-name }}</a>
        {% else %}
          {{ p.partner-name }}
        {% endif %}
      </span>
      
      <br />
      
      {{ p.partner-description }}<br />
      <ul>
        <li>Contact: {{ p.partner-contact }}</li>              
        <li>Tags: {{ p.partner-tags }}</li>
        <li>External: <a href="{{ p.partner-url }}">{{ p.partner-url }}</a></li>      
      </ul>
      
    </li>
  {% endif %}
{% endfor %}
</ul>
