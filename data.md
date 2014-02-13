---
layout: default
title: Social Data Science - Data Sources
all-data-tags: [Development,Education,Homelessness,Hunger,Human trafficking,Miscellaneous,Peace,Poverty]
---
Data Sources
------------

<p class="lead">Public data sources related to social issues</p>

{% comment %}
Note that jekyll only populates site.tags with posts (not regular pages)
{% endcomment %}
{% for tag in page.all-data-tags %}
 - **{{tag}}**:
  {% for p in site.pages %}
    {% if p.layout == "data-source" %}
     {% if p.data-tags contains tag %}
       <a href={{p.data-url}}>{{p.data-name}}</a><br>
       {{p.data-description}}
     {% endif %}
   {% endif %}
  {% endfor %}
{% endfor %}
