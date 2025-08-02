---
layout: default
title: people
permalink: /people/
---
# People

{% for entry in site.data.people %}
  {% assign person = site.pages | where: "id", entry.id | first %}
  {% include person_card.html person=person %}
{% endfor %}

### Alumni

<!-- You can load alumni from a separate list or manually add below -->
<ul>
  <li>Jane Smith (PhD 2023) → Postdoc at MIT</li>
  <li>John Doe (BS 2022) → Graduate Student at Stanford</li>
</ul>