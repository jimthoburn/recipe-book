---
layout: default
title: Recipe Book
---

# Recipe Book

- - -

<ul class="recipes">

  {% assign data_collection = site.collections | where: "label", "recipes" | first %}
  {% assign data_list = data_collection.docs | sort %}

  {% for data in data_list %}
  <li>
    <a href="{{ site.baseurl }}{{ data.url }}">{{ data['title'] }}</a>
  </li>
  {% endfor %}
</ul>
