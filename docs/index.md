---
layout: home
title: series1
exclude: true
---
<ul class="assets">
{% for series in site.series %}
{% assign series = site.series | where_exp: 'item', "item.title" %}
  <li>
         <b>{{ series.name }}</b>
    </a>    
  </li>
{% endfor %}
</ul>
