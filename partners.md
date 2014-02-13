---
layout: default
title: Social Data Science - Potential Partners
---
Potential Partners
------------------

<p class="lead">Relevant organizations, groups, and individuals</p>

<table id="partner-table" class="table table-bordered">
  <thead>
    <th>Name, description, and external link</th>
    <th>Contact</th>
    <th>Tags</th>
  </thead>
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


<script src="/assets/dynatable/jquery.dynatable.js"></script>
<script>
$('#partner-table').dynatable({
    inputs: {
      paginationClass: 'pagination',
      paginationActiveClass: 'active',
      paginationDisabledClass: 'disabled'
    },
    features: {
      paginate: false
    }
});
</script>
