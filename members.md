---
layout: page
title: Members
---

{% for member in site.data.members %}
  <article class="article">
    <ul>
      <li>{{ member.name }}</li>
      <li><img src="{{ member.avatar }}" width="100px"></li>
      <li>{{ member.cursus }}</li>
      <li>
          {%for ligue in site.data.clubs%}
            {%assign footballteam = {{member.footballteam}}%}
            {%assign clubs = ligue[1] | where : key, footballteam %}
            {%for club in clubs %}
              {{club.name}}
            {%endfor%}
          {%endfor%}
      </li>
    </ul>
  </article>
{% endfor%}
