---
layout: home
title: Series 1
exclude: true
---
<img src="https://bafybeihpquzju6nhdktcdbje7xhzbldtqbvrpszckjmfqyf3hcvaxrmnmy.ipfs.nftstorage.link/" max-width="100%" height="auto">
<ul class="assets">
{% for block-1 in site.block-1 %}
{% assign artist = site.artists | where_exp: 'item', "item.title == block-1.author" %}
  <li>
    <img src="{% if block-1.image != null and block-1.image != '' %}{{ block-1.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="block-1/{{ block-1.name | downcase }}">
      <p class="small">Series {{ block-1.series }}, Block {{block-1.block}}<br> Supply {{ block-1.supply }}</p> 
         <b>{{ block-1.name }}</b>
    </a>    
    <p class="small">Artist: {% if artist[0] %}<a href="{{ artist[0].url | relative_url }}">{{ block-1.author }}</a>{% else %}{{ block-1.author }}{% endif %}</p>
  </li>
{% endfor %}
</ul>
