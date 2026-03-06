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

---

## Publications

<ul class="pub-list">

{% assign papers = site.data.publications | where: "type", "paper" | sort: "year" | reverse %}

{% for item in papers %}
<li>

{{ item.authors }}. {{ item.title }}. <em>{{ item.journal }}</em> <strong>{{ item.volume }}</strong>, {{ item.pages }} ({{ item.year }}).

<span class="pub-links">

{% if item.doi %}
<a href="https://doi.org/{{ item.doi }}" class="link-blue">[doi: {{ item.doi }}]</a>
{% endif %}

{% if item.arxiv %}
<a href="https://arxiv.org/abs/{{ item.arxiv }}" class="link-blue">[arXiv: {{ item.arxiv }}]</a>
{% endif %}

{% if item.pdf %}
<a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
{% endif %}

</span>

{% if item.notes %}
<div class="pub-note"><em>({{ item.notes }})</em></div>
{% endif %}

</li>
{% endfor %}

</ul>

---

## Theses

### PhD theses

<ul class="pub-list">

{% assign phd = site.data.publications | where: "type", "phd_thesis" | sort: "year" | reverse %}

{% for item in phd %}
<li>

{{ item.authors }}. <em>{{ item.title }}</em>. PhD thesis, {{ item.institution }} ({{ item.year }}).

{% if item.pdf %}
<a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
{% endif %}

{% if item.notes %}
<div class="pub-note"><em>({{ item.notes }})</em></div>
{% endif %}

</li>
{% endfor %}

</ul>

### Master's theses

<ul class="pub-list">

{% assign masters = site.data.publications | where: "type", "masters_thesis" | sort: "year" | reverse %}

{% for item in masters %}
<li>

{{ item.authors }}. <em>{{ item.title }}</em>. Master's thesis, {{ item.institution }} ({{ item.year }}).

{% if item.pdf %}
<a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
{% endif %}

{% if item.notes %}
<div class="pub-note"><em>({{ item.notes }})</em></div>
{% endif %}

</li>
{% endfor %}

</ul>

### Bachelor's theses

<ul class="pub-list">

{% assign bachelors = site.data.publications | where: "type", "bachelors_thesis" | sort: "year" | reverse %}

{% for item in bachelors %}
<li>

{{ item.authors }}. <em>{{ item.title }}</em>. Bachelor's thesis, {{ item.institution }} ({{ item.year }}).

{% if item.pdf %}
<a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
{% endif %}

{% if item.notes %}
<div class="pub-note"><em>({{ item.notes }})</em></div>
{% endif %}

</li>
{% endfor %}

</ul>

---

## Internal reports

<ul class="pub-list">

{% assign reports = site.data.publications | where: "type", "report" | sort: "year" | reverse %}

{% for item in reports %}
<li>

{{ item.authors }}. <em>{{ item.title }}</em>. {{ item.institution }} ({{ item.year }}).

{% if item.pdf %}
<a href="{{ item.pdf }}" class="link-blue">[pdf]</a>
{% endif %}

{% if item.notes %}
<div class="pub-note"><em>({{ item.notes }})</em></div>
{% endif %}

</li>
{% endfor %}

</ul>