---
layout: home
title: Home
exclude: true
---
<img src={{"assets/rarebtc-banner.gif"}} alt="rare btc banner" max-width="100%" height="auto">
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
