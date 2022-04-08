---
layout: home
title: Home
exclude: true
---
<img src={{'https://bafybeihpquzju6nhdktcdbje7xhzbldtqbvrpszckjmfqyf3hcvaxrmnmy.ipfs.nftstorage.link/'}} style=height="60" width="200">
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
