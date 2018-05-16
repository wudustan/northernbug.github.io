---
layout: page
title: Members
permalink: /members/
---


## Current Members

<table>
{% for member in site.data.members %}

    {% capture modulo %}{{ forloop.index | modulo: 3 }}{% endcapture %}
    {% if modulo == '1' %}
      <tr>
    {% endif %}
    <td align="center">
      {% if member.github %}
        {% avatar user=member.github size=100 %}<br>
      {% else %}
        <img src="/assets/no-github.png"><br>
      {% endif %}
      <strong>{{ member.name }}</strong><br>
      {{ member.institute }}<br>
      {{ member.email }}<br>
      <a href="{{member.website}}">web</a> | twitter
    </td>
    {% if modulo == '0' or forloop.last %}
      </tr>
      {% endif %}
{% endfor %}
</table>

<!---
To Add yourself to the members table:
in the data directory you need to add yourself to the members.yml file:

- github: markdunning
  name: Mark Dunning
  institute: Sheffield University Bioinformatics Core
  email: m.j.dunning@sheffield.ac.uk


-->


## Alumini

<table>
{% for member in site.data.alumni %}
  {% capture modulo %}{{ forloop.index | modulo: 3 }}{% endcapture %}
    {% if modulo == '1' %}
      <tr>
    {% endif %}
    <td align="center">
      {% if member.github %}
        {% avatar user=member.github size=100 %}<br>
        {% else %}
        <img src="/assets/no-github.png"><br>
      {% endif %}
      <strong>{{ member.name }}</strong><br>
      {{ member.institute }}<br>
      {{ member.email }}<br>
      <a href="{{member.website}}">{{member.website}}</a>
     </td>
    {% if modulo == '0' or forloop.last %}
    </tr>
    {% endif %}
{% endfor %}
</table>
