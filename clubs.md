---
layout: page
title: Clubs
---


{% for ligue in site.data.clubs %}
      {% for club in ligue[1]%}
        {{club.key}}
        {{club.name}}
      {% endfor %}
{% endfor %}

##affichage du json en brut
