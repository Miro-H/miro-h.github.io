---
permalink: /
excerpt: "PhD student in applied crypto @ UCSD. Hacker."
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

My research interests are in the intersection of applied cryptography, system security, and privacy. I'm excited about using mathematical techniques for cryptanalysis. I leverage attacks to identify the root causes of cryptography failures in practice, and then build or improve systems to address these failures.

I'm fortunate to work with many amazing people including my PhD advisor @ UC San Diego [Nadia Heninger](https://cseweb.ucsd.edu/~nadiah/){:target="_blank"}, [Kenny Paterson](https://appliedcrypto.ethz.ch/){:target="_blank"}, [Matilda Backendal](https://mbackendal.github.io/){:target="_blank"}, and many other outstanding internal and external collaborators.

## Selected Publications

<ul>
{%- assign papers = site.papers | reverse -%}
{%- for post in papers -%}
    {% if post.spotlight == 'yes' %}
        {%- include archive-single-about.html -%}
    {% endif %}
{%- endfor -%}
</ul>

[Click here for all publications...](/publications/)

## Selected Achievements

<ul>
{% for achievement in site.data.achievements %}
    {% if achievement.spotlight == 'yes' %}
        <li>{{ achievement.text | markdownify }}</li>
    {% endif %}
{% endfor %}
</ul>

[Click here for the full CV](/cv/)
