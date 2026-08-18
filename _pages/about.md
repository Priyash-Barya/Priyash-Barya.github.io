---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am currently a PhD student at the University of Illinois Urbana Champaign (UIUC) working under Prof. Elizabeth Goldschmidt. I am an experimentalist working in the area of quantum optics and interested in building technogies for future quantum information processing and networking. Previously, I received my MS degree from UIUC working with Prof. Brian Cunningham on using plasmonic-photonic coupling to enhance biosensing. 

Research Experience
======
Below are the main threads of my research. Where available, the title of each links directly to a representative publication (the <i class="fa fa-link" aria-hidden="true"></i> icon links to the item's own page).

{% include base_path %}

{% for post in site.portfolio %}
  {% include archive-single.html %}
{% endfor %}
