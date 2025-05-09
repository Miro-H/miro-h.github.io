---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

## Research Interests
My research interests are in the intersection of applied cryptography, system security, and privacy. I am excited about using mathematical techniques for cryptanalysis. I leverage attacks to identify the root causes of cryptography failures in practice, and then build or improve systems to address these failures.

## Education

- MSc ETH Zurich &ndash; EPF Lausanne in Computer Science Major in Cyber Security (short: MSc ETH EPF CS)
- BSc ETH Zurich in Computer Science (short: BSc ETH CS)

Ongoing:

- PhD at UCSD advised by [Nadia Heninger](https://cseweb.ucsd.edu/~nadiah/) (Fall 2022 - today)

## Publications

Papers published in peer-reviewed proceedings:
<ul>
{%- assign papers = site.papers | reverse -%}
{%- for post in papers -%}
    {% if post.published == 'yes' %}
        {%- include archive-single-cv.html -%}
    {% endif %}
{%- endfor -%}
</ul>

Unreviewed/pre-print papers:
<ul>
{%- assign papers = site.papers | reverse -%}
{%- for post in papers -%}
    {% unless post.published == 'yes' %}
        {%- include archive-single-cv.html -%}
    {% endunless %}
{%- endfor -%}
</ul>

Articles:
<ul>
{%- assign articles = site.articles | reverse -%}
{%- for post in articles -%}
    {%- include archive-single-cv.html -%}
{%- endfor -%}
</ul>

\*_first author(s)_

## Talks

<ul>
{%- assign talks = site.talks | reverse -%}
{%- for post in talks -%}
    {%- include archive-single-talk-cv.html -%}
{%- endfor -%}
</ul>

## Academic Service

<ul>
{% for service in site.data.academic_service %}
	<li>{{ service | markdownify }}</li>
{% endfor %}
</ul>

## Department Service

<ul>
{% for service in site.data.department_service %}
	<li>{{ service | markdownify }}</li>
{% endfor %}
</ul>

## Teaching

<ul>
{% for lesson in site.data.teaching %}
        <li>{{ lesson | markdownify }}</li>
{% endfor %}
</ul>

## Professional experience

<ul>
{% for exp in site.data.professional_experience %}
        <li>{{ exp | markdownify }}</li>
{% endfor %}
</ul>

## Achievements

<ul>
{% for achievement in site.data.achievements %}
        <li>{{ achievement.text | markdownify }}</li>
{% endfor %}
</ul>
