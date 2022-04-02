---
layout: home
title: Home
exclude: true
---

<ul class="assets">
{% for series in site.series %}<p Supply {{ sub.supply }}</p>
{% assign artist = site.artists | where_exp: 'item', "item.title == series.author" %}
  <li>
    <img src="{% if series.image != null and series.image != '' %}{{ series.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="series/{{ series.name | downcase }}">
      <p class="small">Card {{forloop.index}}</p>
      <b>{{ series.name }}</b>
    </a>    
    <p class="small">Artist: {% if artist[0] %}<a href="{{ artist[0].url | relative_url }}">{{ series.author }}</a>{% else %}{{ series.author }}{% endif %}</p>
  </li>
{% endfor %}
</ul>
