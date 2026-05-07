---
layout: default
title: people
permalink: /people/
---


# People

{% for entry in site.data.people.current %}
  {% assign person = site.pages | where: "id", entry.id | first %}
  {% include member_card.html person=person %}
{% endfor %}

# Alumni

<div class="alumni-list">
{% for entry in site.data.people.alumni %}
  {% assign person = site.pages | where: "id", entry.id | first %}

  <div class="alumni-entry">
    <strong>
      {% if person.linkedin %}
        <a href="{{ person.linkedin }}" target="_blank" rel="noopener noreferrer">{{ person.myname }}</a>
      {% else %}
        {{ person.myname }}
      {% endif %}
    </strong>

    {% if person.start_date or person.end_date %}
      <span>
        — {{ person.start_date }}{% if person.end_date %}–{{ person.end_date }}{% endif %}
      </span>
    {% endif %}

    {% if person.next_position %}
      <br>
      <span>Next position: {{ person.next_position }}</span>
    {% endif %}
  </div>

{% endfor %}
</div>

{% endif %}



<!--
### Alumni
You can load alumni from a separate list or manually add below 
<ul>
  <li>Jane Smith (PhD 2023) → Postdoc at MIT</li>
  
</ul>

-->