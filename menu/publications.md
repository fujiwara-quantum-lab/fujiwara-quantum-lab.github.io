---
layout: default
title: Publications
permalink: /publications/
---

- [Publications](#publications)
- [Theses](#theses)
  - [PhD theses](#phd-theses)
  - [Master's theses](#masters-theses)
  - [Bachelor's theses](#bachelors-theses)
- [Internal reports](#internal-reports)

## Publications

<div class="pub-list">

{% assign papers = site.data.publications | where: "type", "paper" | sort: "year" | reverse %}
{% for item in papers %}
  <div class="pub-entry">
    <div class="pub-authors">{{ item.authors }}</div>
    <div class="pub-title">{{ item.title }}</div>
    {% if item.journal %}
      <div class="pub-journal">
        <em>{{ item.journal }}</em>{% if item.volume %} <strong>{{ item.volume }}</strong>{% endif %}{% if item.pages %}, {{ item.pages }}{% endif %} ({{ item.year }})
      </div>
    {% elsif item.year %}
      <div class="pub-journal">({{ item.year }})</div>
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

    {% if item.notes and item.notes != "" %}
      <div class="pub-note"><em>({{ item.notes }})</em></div>
    {% endif %}
  </div>
{% endfor %}

</div>

## Theses

### PhD theses

<div class="pub-list">

{% assign phd = site.data.publications | where: "type", "phd_thesis" | sort: "year" | reverse %}
{% for item in phd %}
  <div class="pub-entry">
    <div class="pub-authors">{{ item.authors }}</div>
    <div class="pub-title">{{ item.title }}</div>
    <div class="pub-journal"><em>PhD thesis</em>, {{ item.institution }} ({{ item.year }})</div>

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

    {% if item.notes and item.notes != "" %}
      <div class="pub-note"><em>({{ item.notes }})</em></div>
    {% endif %}
  </div>
{% endfor %}

</div>

### Master's theses

<div class="pub-list">

{% assign masters = site.data.publications | where: "type", "masters_thesis" | sort: "year" | reverse %}
{% for item in masters %}
  <div class="pub-entry">
    <div class="pub-authors">{{ item.authors }}</div>
    <div class="pub-title">{{ item.title }}</div>
    <div class="pub-journal"><em>Master's thesis</em>, {{ item.institution }} ({{ item.year }})</div>

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

    {% if item.notes and item.notes != "" %}
      <div class="pub-note"><em>({{ item.notes }})</em></div>
    {% endif %}
  </div>
{% endfor %}

</div>

### Bachelor's theses

<div class="pub-list">

{% assign bachelors = site.data.publications | where: "type", "bachelors_thesis" | sort: "year" | reverse %}
{% for item in bachelors %}
  <div class="pub-entry">
    <div class="pub-authors">{{ item.authors }}</div>
    <div class="pub-title">{{ item.title }}</div>
    <div class="pub-journal"><em>Bachelor's thesis</em>, {{ item.institution }} ({{ item.year }})</div>

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

    {% if item.notes and item.notes != "" %}
      <div class="pub-note"><em>({{ item.notes }})</em></div>
    {% endif %}
  </div>
{% endfor %}

</div>

## Internal reports

<div class="pub-list">

{% assign reports = site.data.publications | where: "type", "report" | sort: "year" | reverse %}
{% for item in reports %}
  <div class="pub-entry">
    <div class="pub-authors">{{ item.authors }}</div>
    <div class="pub-title">{{ item.title }}</div>
    <div class="pub-journal"><em>Internal report</em>{% if item.institution %}, {{ item.institution }}{% endif %} ({{ item.year }})</div>

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

    {% if item.notes and item.notes != "" %}
      <div class="pub-note"><em>({{ item.notes }})</em></div>
    {% endif %}
  </div>
{% endfor %}

</div>