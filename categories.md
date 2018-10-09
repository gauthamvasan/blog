---
layout: blank
permalink: /categories/
title: Categories
---


<div id="archives">
    <br> <br>
<h1>All Posts by Category</h1>
{% for category in site.categories %}
  <div class="6u 12u$(small)">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>    
    <h2 class="category-head">{{ category_name }}</h2>
    <a name="{{ category_name | slugize }}"></a>
        {% for post in site.categories[category_name] %}
        <li><article class="archive-item">
          <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a> written on {{ post.date | date_to_string }}</h4> 
        </article></li>
    <br>
    {% endfor %}
  </div>
{% endfor %}
</div>