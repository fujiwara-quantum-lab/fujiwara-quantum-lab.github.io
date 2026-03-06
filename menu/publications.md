---
layout: default
title: Publications
permalink: /publications/
---

# Publications

<div class="pub-list">

{% assign papers = site.data.publications | where: "type", "paper" | sort: "year" | reverse %}

{% for item in papers %}
<div class="pub-entry">

  <div class="pub-title">{{ item.title }}</div>

  <div class="pub-authors">
    {{ item.authors }}.
    {% if item.journal %}
      <em>{{ item.journal }}</em>{% if item.volume %} <strong>{{ item.volume }}</strong>{% endif %}{% if item.pages %}, {{ item.pages }}{% endif %} ({{ item.year }})
    {% elsif item.year %}
      ({{ item.year }})
    {% endif %}
  </div>

  {% if item.notes and item.notes != "" %}
    <div class="pub-note"><em>({{ item.notes }})</em></div>
  {% endif %}

  {% if item.doi or item.arxiv or item.pdf %}
<div class="pub-links">

{% if item.doi %}
<a href="https://doi.org/{{ item.doi }}" class="link-blue">[doi: {{ item.doi }}]</a>
{% endif %}

{% if item.arxiv %}
<a href="https://arxiv.org/abs/{{ item.arxiv }}" class="link-blue">[arXiv: {{ item.arxiv }}]</a>
{% endif %}

{% if item.pdf %}
<a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
{% endif %}

</div>
{% endif %}

</div>
{% endfor %}

</div>

# Theses

## PhD theses

<div class="thesis-list">

{% assign phd = site.data.publications | where: "type", "phd_thesis" | sort: "year" | reverse %}

{% for item in phd %}
<div class="thesis-entry">
  {{ item.authors }}. <em>{{ item.title }}</em>, {{ item.institution }} ({{ item.year }})
  {% if item.pdf %}
    <a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
  {% endif %}
  {% if item.doi %}
    <a href="https://doi.org/{{ item.doi }}" class="link-blue">[doi]</a>
  {% endif %}
  {% if item.arxiv %}
    <a href="https://arxiv.org/abs/{{ item.arxiv }}" class="link-blue">[arXiv]</a>
  {% endif %}
</div>
{% endfor %}

</div>

## Master's theses

<div class="thesis-list">

{% assign masters = site.data.publications | where: "type", "masters_thesis" | sort: "year" | reverse %}

{% for item in masters %}
<div class="thesis-entry">
  {{ item.authors }}. <em>{{ item.title }}</em>, {{ item.institution }} ({{ item.year }})
  {% if item.pdf %}
    <a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
  {% endif %}
  {% if item.doi %}
    <a href="https://doi.org/{{ item.doi }}" class="link-blue">[doi]</a>
  {% endif %}
  {% if item.arxiv %}
    <a href="https://arxiv.org/abs/{{ item.arxiv }}" class="link-blue">[arXiv]</a>
  {% endif %}
</div>
{% endfor %}

</div>

## Bachelor's theses

<div class="thesis-list">

{% assign bachelors = site.data.publications | where: "type", "bachelors_thesis" | sort: "year" | reverse %}

{% for item in bachelors %}
<div class="thesis-entry">
  {{ item.authors }}. <em>{{ item.title }}</em>, {{ item.institution }} ({{ item.year }})
  {% if item.pdf %}
    <a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
  {% endif %}
  {% if item.doi %}
    <a href="https://doi.org/{{ item.doi }}" class="link-blue">[doi]</a>
  {% endif %}
  {% if item.arxiv %}
    <a href="https://arxiv.org/abs/{{ item.arxiv }}" class="link-blue">[arXiv]</a>
  {% endif %}
</div>
{% endfor %}

</div>

# Internal reports

<div class="thesis-list">

{% assign reports = site.data.publications | where: "type", "report" | sort: "year" | reverse %}

{% for item in reports %}
<div class="thesis-entry">
  {{ item.authors }}. <em>{{ item.title }}</em>{% if item.institution %}, {{ item.institution }}{% endif %} ({{ item.year }})
  {% if item.pdf %}
    <a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
  {% endif %}
  {% if item.doi %}
    <a href="https://doi.org/{{ item.doi }}" class="link-blue">[doi]</a>
  {% endif %}
  {% if item.arxiv %}
    <a href="https://arxiv.org/abs/{{ item.arxiv }}" class="link-blue">[arXiv]</a>
  {% endif %}
  {% if item.notes and item.notes != "" %}
    <span class="report-note"><em>({{ item.notes }})</em></span>
  {% endif %}
</div>
{% endfor %}

</div>