---
layout: blank
permalink: /categories/
title: Categories
---

<section>
<div id="archives">
    <br> <br>
<h1>All Posts by Category</h1>
{% for category in site.categories %}
  <div class="6u 12u$(small)">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>
          <header class="major">
        <h2 class="category-head">{{ category_name }}</h2>
    </header>    
    <a name="{{ category_name | slugize }}"></a>
      <ul class="alt">
        {% for post in site.categories[category_name] %}
        <li><article class="archive-item">
          <b><a class="post-link" href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a> written on {{ post.date | date_to_string }}</b> 
        </article></li>
    {% endfor %}
      </ul>
  </div>
{% endfor %}
</div>
</section>