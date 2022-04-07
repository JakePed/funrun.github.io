---
layout: home
title: Series 1

---
<img src="https://bafybeiaelbcwjlihme66n23jfbw4j2vcgmzqg6nt2oql2xd3a5mf72vpsu.ipfs.nftstorage.link/" alt="rare btc banner" max-width="100%" height="auto">
<ul class="assets">
{% for card in site.cards1 %}
{% assign artist = site.artists | where_exp: 'item', "item.title == cards1.author" %}
  <li>
    <img src="{% if cards1.image != null and cards1.image != '' %}{{ cards1.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="card/{{ cards1.name | downcase }}">
      <p class="small">Series {{ cards1.series }}, Card {{cards1.card}}<br> Supply {{ cards1.supply }}</p> 
         <b>{{ cards-1.name }}</b>
    </a>    
  </li>
{% endfor %}
</ul>
