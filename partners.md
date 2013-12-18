---
layout: default
title: Social Data Science - Potential Partners
---
Potential Partners
--------------------------------

Relevant organizations, groups, and individuals:

<table>
  <tr>
    <th>Name, description, and external link</th>
    <th>Contact</th>    
    <th>Tags</th>        
  </tr>
  {% for p in site.pages %}
    {% if p.layout == 'partner' %}
      <tr>
        <td class="partner-name">
          {% if p.is-full-page %}
            <a class="partner-name" href="{{ p.url }}">{{ p.partner-name }}</a>
          {% else %}
            <span class="partner-name">{{ p.partner-name }}</span>
          {% endif %}
          <br />
          {{ p.partner-description }}<br />
          <a href="{{ p.partner-url }}">{{ p.partner-url }}</a>
        </td>
        <td class="partner-contact">{{ p.partner-contact }}</td>              
        <td class="partner-tags">{{ p.partner-tags }}</td>
      </tr>
    {% endif %}
  {% endfor %}
</table>
