---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
I am currently a PhD student at the University of Illinois Urbana Champaign (UIUC) working under Prof. Elizabeth Goldschmidt. I am an experimentalist working in the area of quantum optics and currently interested in building technogies for future quantum information processing and networking. Previously, I received my MS degree from UIUC working with Prof. Brian Cunningham on using plasmonic-photonic coupling to enhance biosensing. 

My contact information is - pbarya2[at]illinois.edu


Research Experience
======
{% include base_path %}
{% for post in site.portfolio %}
  {% if post.header.teaser %}
    {% capture teaser %}{{ post.header.teaser }}{% endcapture %}
  {% else %}
    {% assign teaser = site.teaser %}
  {% endif %}

  <div class="list__item">
    <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
      <h2 class="archive__item-title" itemprop="headline">{{ post.title }}</h2>

      {% if post.excerpt and site.read_more != 'enabled' %}
        <p class="archive__item-excerpt" itemprop="description">{{ post.excerpt | markdownify }}</p>
      {% elsif post.excerpt and site.read_more == 'enabled' %}
        <p class="archive__item-excerpt" itemprop="description">{{ post.excerpt | markdownify | remove: '<p>' | remove: '</p>' }}<strong><a href="{{ base_path }}{{ post.url }}" rel="permalink"> Read more</a></strong></p>
      {% endif %}
    </article>
  </div>
{% endfor %}
