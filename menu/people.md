---
layout: default
title: people
permalink: /people/
---

{% for entry in site.data.people %}
  {% assign person = site.pages | where: "id", entry.id | first %}
  {% include member_card.html person=person %}
{% endfor %}

### Alumni

<!-- You can load alumni from a separate list or manually add below -->
<ul>
<!-- 
  <li>Jane Smith (PhD 2023) → Postdoc at MIT</li>
  -->
</ul>