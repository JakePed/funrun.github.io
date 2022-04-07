---
layout: home
title: Series 1
---
<img src="https://bafybeiaelbcwjlihme66n23jfbw4j2vcgmzqg6nt2oql2xd3a5mf72vpsu.ipfs.nftstorage.link/" alt="rare btc banner" max-width="100%" height="auto">
<ul class="assets">
{% for card-1 in site.card-1 %}
{% assign artist = site.artists | where_exp: 'item', "item.title == card-1.author" %}
  <li>
    <img src="{% if card-1.image != null and card-1.image != '' %}{{ card-1.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="card-1/{{ card-1.name | downcase }}">
      <p class="small">Series {{ card-1.series }}, Card {{card-1.card}}<br> Supply {{ card-1.supply }}</p> 
         <b>{{ card-1.name }}</b>
    </a>    
    <p class="small">Artist: {% if artist[0] %}<a href="{{ artist[0].url | relative_url }}">{{ card-1.author }}</a>{% else %}{{ card-1.author }}{% endif %}</p>
  </li>
{% endfor %}
</ul>
