---
layout: page
permalink: /categories/
title: Categories
---


<div id="archives">
{% for category in site.categories %}
  <div class="6u 12u$(small)">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>    
    <h2 class="category-head">{{ category_name }}</h2>
    <a name="{{ category_name | slugize }}"></a>
    <ul class="alt">
        {% for post in site.categories[category_name] %}
        <li><article class="archive-item">
          <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a> written on {{ post.date | date_to_string }}</h4> 
          <p>{{post.subtitle}}</p>
        </article></li>        
    </ul>
        {% endfor %}
  </div>
{% endfor %}
</div>