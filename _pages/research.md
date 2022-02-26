---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.research reversed %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
  {% include archive-single.html %}
{% endfor %}
