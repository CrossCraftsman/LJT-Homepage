---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% for category in site.publication_category %}
  {% assign title = category[1].title %}
  {% assign cat = category[0] %}
  <h2>{{ title }}</h2>
  <ul>
  {% for post in site.publications reversed %}
    {% if post.category == cat %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}
