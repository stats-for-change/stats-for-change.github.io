---
layout: default
title: Social Data Science - Projects
---
Projects
--------------------------------

This page contains information on some of our projects related to applying data science to social domains.

- [GreatNonprofits](/projects/greatnonprofits.html)<br>
  Understanding the value of feedback from beneficiaries; constructing a meaningful nonprofit rating when feedback comes from disparate sources
- [Stanford Center for Education Policy Analysis](/projects/stanford-cepa.html)<br>
  Analyzing small school district data

<table>
    <tr><th>Organization Name</th><th>Short Description</th></tr>
{% for p in site.pages %}
  {% if p.category == 'projects' %}
    {% comment %} 
    The below uses the convention of ' - ' between title elements.
    Probably better to do this more robustly if we stick with Jekyll 
    {% endcomment %}
    <tr><td><a href={{p.url}}>{{p.title | split: ' - ' | last}}</a></td><td>{{p.description}}</td></tr>
  {% endif %}
{% endfor %}
</table>
