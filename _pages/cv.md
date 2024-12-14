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

- Organizing the [Cryptographic Applications Workshop (CAW) at Eurocrypt 2024](https://caw.cryptanalysis.fun/)
- Organizing the [Workshop on Attacks in Cryptography 6 (WAC6) at CRYPTO 2023](https://wac6.cryptanalysis.fun/)

## Professional experience

- Research assisstant at the [Privacy Preserving Systems Lab](https://pps-lab.com/) of ETH Zurich
  - Content valuating and improving Fully Homomorphic Encryption (FHE) tool support
- Intern at [DSwiss AG](https://www.securesafe.com/en/business/overview) (2016)
  - Adapting and extending automated server configurations, load and performance testing, E2E tests, replacing the company's telephone system.

## Achievements

- [Google PhD Fellowship](https://research.google/programs-and-events/phd-fellowship/recipients/) 2024
- [Distinguished paper award](https://www.ieee-security.org/TC/SP2023/program-awards.html) at IEEE S&P 2023.
- [ETH Medal](https://ethz.ch/en/the-eth-zurich/education/awards/eth-medal/outstanding-master-theses.html): Award for outstanding master's thesis.
- [Global Young Scientist Summit 2022](https://www.nrf.gov.sg/gyss/home): Nomination as ETH representative for the CS department.
- [European Cyber Security Challenge](https://europeancybersecuritychallenge.eu/): triple qualification for the Swiss National Team (2016, 2017, 2019), and team coach (2021, 2022)
- [SwissSkills Expert](https://www.swiss-skills.ch/de): Expert for the Cyber Security Trait of the Swiss national championship for professions in 2022 and 2023.
- [ISSS Excellence Award](https://isss.ch/veranstaltungeb-kurse/isss-excellence-award-2022/): Award for the best thesis in the field of information security in Switzerland in 2022.
- [ICON](https://icon.ngo/challenge-ctf/): achieved first place with the team "sw1ss" in the 2018 final
- [Swiss Olympiads of Informatics](https://soi.ch/): double participation (2014, 2015)
- Best high school graduate of the year 2015 from the Neue Kantonsschule Aarau.
