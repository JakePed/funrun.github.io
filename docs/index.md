---
layout: home
title: Home
exclude: true
---
<img src="https://bafybeidfwnuaxycyypvgtnornhcztrirngnv5nrm6oevpfu66masij2jwa.ipfs.nftstorage.link/" alt="rare btc banner" max-width="100%" height="auto">
<ul class="assets">
{% for card in site.cards %}
{% assign artist = site.artists | where_exp: 'item', "item.title == cards.author" %}
  <li>
    <img src="{% if cards.image != null and cards.image != '' %}{{ cards.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="series/1/cards/{{ cards.name | downcase }}">
      <p class="small">Series {{ cards.series }}, Cards {{cards.card}}<br> Supply {{ cards.supply }}</p> 
         <b>{{ card.name }}</b>
    </a>    
    <p class="small">Artist: {% if artist[0] %}<a href="{{ artist[0].url | relative_url }}">{{ cards.author }}</a>{% else %}{{ cards.author }}{% endif %}</p>
  </li>
{% endfor %}
</ul>
