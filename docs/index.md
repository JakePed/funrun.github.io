---
layout: home
title: Home
exclude: true
---

<ul class="assets">
{% for card in site.card %}
{% assign artist = site.artists | where_exp: 'item', "item.title == card.author" %}
  <li>
    <img src="{% if card.image != null and card.image != '' %}{{ card.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="card/{{ card.name | downcase }}">
      <p class="small">Series {{ card.series }}, Card {{card.card}} <b> Supply {{ card.supply }}<b></p>
      
        <b>{{ card.name }}</b>
    </a>    
    <p class="small">Artist: {% if artist[0] %}<a href="{{ artist[0].url | relative_url }}">{{ card.author }}</a>{% else %}{{ card.author }}{% endif %}</p>
  </li>
{% endfor %}
</ul>
