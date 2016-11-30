---
layout: page
title: Les boucles
---

#Les boucles Jekyll

Une boucle pour créer un menu :

    <ul>
      {% for p in site.pages %}
        <li>
          <a href="{{ p.url }}">{{ p.title }}</a>
        </li>
      {% endfor %}
    </ul>
