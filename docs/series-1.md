---
layout: home
title: Series 1

---
<img src="https://bafybeiaelbcwjlihme66n23jfbw4j2vcgmzqg6nt2oql2xd3a5mf72vpsu.ipfs.nftstorage.link/" alt="rare btc banner" max-width="100%" height="auto">
<ul class="assets">
{% for card in site.cards-1 %}
{% assign artist = site.artists | where_exp: 'item', "item.title == cards-1.author" %}
  <li>
    <img src="{% if cards-1.image != null and cards-1.image != '' %}{{ cards-1.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="cards-1/{{ cards-1.name | downcase }}">
      <p class="small">Series {{ cards-1.series }}, Card {{cards-1.card}}<br> Supply {{ cards-1.supply }}</p> 
         <b>{{ cards-1.name }}</b>
    </a>    
    <p class="small">Artist: {% if artist[0] %}<a href="{{ artist[0].url | relative_url }}">{{ cards-1.author }}</a>{% else %}{{ cards-1.author }}{% endif %}</p>
  </li>
{% endfor %}
</ul>
