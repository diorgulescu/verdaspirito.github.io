---
layout: page
title: Posts
updated: 2021-01-18 09:00:00 +0200
---
<p>
<h3>Austria și Slovenia, via Veneția (iunie 2015)</h3>
{% for post in site.categories.austriaslovenia reversed%}
  {% unless post.draft %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    {% unless forloop.first %}</ul>{% endunless %}
    <ul>
    {% assign date = currentdate %}
  {% endif %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% if forloop.last %}</ul>{% endif %}
  {% endunless %}
{% endfor %}
</p>
<p>
<h3>Prin Elveția și Italia (iunie 2016)</h3>
{% for post in site.categories.elvetiaitalia reversed%}
  {% unless post.draft %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    {% unless forloop.first %}</ul>{% endunless %}
    <ul>
    {% assign date = currentdate %}
  {% endif %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% if forloop.last %}</ul>{% endif %}
  {% endunless %}
{% endfor %}
</p>
