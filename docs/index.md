---
layout: home
title: Home
exclude: true
---
 <a href="/series-1">
  <img src={{'assets/rarebtc-banner.gif'}} style=height="60" width="200">
</a>    
<ul class="assets">
{% for series in site.series %}

  <li>
    <img src="{% if series.image != null and series.image != '' %}{{ series.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="/{{ series.name | downcase }}">
         <b>{{ series.name }}</b>
    </a>    
  </li>
{% endfor %}
</ul>
