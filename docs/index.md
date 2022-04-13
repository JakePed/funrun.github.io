---
layout: home
title: Home
exclude: true
---
<img src="https://bafybeiaelbcwjlihme66n23jfbw4j2vcgmzqg6nt2oql2xd3a5mf72vpsu.ipfs.dweb.link/" max-width="100%" height="auto">

<b> Currently cards will drop in batches of 7 on a weekly basis <b>

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
