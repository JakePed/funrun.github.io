---
layout: home
title: Home
exclude: true
---
<img src="https://bafybeifmsiihs3gb5hx6vddfkgpk2wlpvuq424stzyy4ybrrod4lwb7hde.ipfs.nftstorage.link/" max-width="100%" height="auto">

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
