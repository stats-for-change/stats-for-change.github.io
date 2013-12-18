---
layout: default
title: Social Data Science - Data Sources
all-tags: [development,education]
---
Data Sources
--------------------------------

Public data sources related to social issues:

{% comment %}
Note that jekyll only populates site.tags with posts (not regular pages)
{% endcomment %}
{% for tag in page.all-tags %}
 - **{{tag}}**:
  {% for p in site.pages %}
    {% if p.layout == "data-source" %}
     {% if p.tags contains tag %}
       <a href={{p.url}}>{{p.name}}</a><br>
       {{p.description}}
     {% endif %}
   {% endif %}
  {% endfor %}
{% endfor %}

- __Education__
    - [PISA](http://www.oecd.org/pisa/)<br>
      "The PISA data consists of test results for 15 year olds across approximately 60 countries, testing at least 5000 students per country on reading, mathematics and science skills."
    - [National Center for Educational Statistics](http://nces.ed.gov/edat/)<br>
      Large database with downloadable data from several large studies on education in the US
- __Human trafficking__
    - [UN Office on Drugs and Crime](http://www.unodc.org/cld/)<br>
      Small global database on human trafficking cases
    - [University of Michigan: Human Trafficking Database](https://www.law.umich.edu/clinical/HuTrafficCases/Pages/searchdatabase.aspx)<br>
      Human trafficking cases in the US.
- __Global development__
    - [UNDP Human Development Index](http://hdr.undp.org/en/data/profiles/)<br>
      Huge database of International Human Development Indicator(s), Gender Inequality Index and Multidimensional Poverty Index, insearchable by country or by indicator.  Also contains great graphs and maps comparing trends over time and cross-national data.
    - [Africa Open Data](http://africaopendata.org/)<br>
      The Open Africa Platform initiative aims to be largest repository of Data on the Africa Continent. 
    - [World Bank](http://data.worldbank.org/)<br>
      Open datasets that are related to the financing and delivery of public goods, works, and services, including procurement and contracting. Also has World Development Indicators.
    - [AidData](http://aiddata.org/)<br>
      Searchable database of nearly one million past and present aid activities around the world.
    - [PeaceBuildingData](peacebuildingdata.org)
- __Miscellaneous__
    - [San Francisco Data](https://data.sfgov.org/)<br>
      The Open Data Portal is is provided by the City and County of San Francisco to enhance open government, transparency, and accountability by improving access to data.
    - [Quandl](http://www.quandl.com)<br>
      "Search over 7,000,000 financial, economic, and social datasets"
    - [Gdelt](http://gdelt.utdallas.edu/)<br>
      Global database of events, language, and tone.
    - [datamob.org/datasets](http://datamob.org/datasets)
    - [datahub.io](http://datahub.io)
