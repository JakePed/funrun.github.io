---
layout: home
title: Home
exclude: true
---
<img src="https://bafybeibk4sry3qtsshilw6m5t7ri4gacjy7nxfx7mxupxh6tty5tqznr4a.ipfs.nftstorage.link/" alt="rare btc banner" max-width="100%" height="auto">
<ul class="assets">
{% for card in site.card %}
{% assign artist = site.artists | where_exp: 'item', "item.title == card.author" %}
  <li>
    <img src="{% if card.image != null and card.image != '' %}{{ card.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="card/{{ cards.name | downcase }}">
      <p class="small">Series {{ card.series }}, Card {{card.card}}<br> Supply {{ card.supply }}</p> 
         <b>{{ card.name }}</b>
    </a>    
    <p class="small">Artist: {% if artist[0] %}<a href="{{ artist[0].url | relative_url }}">{{ card.author }}</a>{% else %}{{ card.author }}{% endif %}</p>
  </li>
{% endfor %}
</ul>
