---
layout: home
title: Series 2
---
<img src="https://bafybeiaelbcwjlihme66n23jfbw4j2vcgmzqg6nt2oql2xd3a5mf72vpsu.ipfs.nftstorage.link/" alt="rare btc banner" max-width="100%" height="auto">
<ul class="assets">
{% for card-1 in site.card-2 %}
{% assign artist = site.artists | where_exp: 'item', "item.title == card-2.author" %}
  <li>
    <img src="{% if card-2.image != null and card-2.image != '' %}{{ card-2.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="card-2/{{ card-2.name | downcase }}">
      <p class="small">Series {{ card-2.series }}, Card {{card-2.card}}<br> Supply {{ card-2.supply }}</p> 
         <b>{{ card-2.name }}</b>
    </a>    
    <p class="small">Artist: {% if artist[0] %}<a href="{{ artist[0].url | relative_url }}">{{ card-2.author }}</a>{% else %}{{ card-2.author }}{% endif %}</p>
  </li>
{% endfor %}
</ul>
