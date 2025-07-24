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

<button type="button" class="btn border border-white" onclick="window.location.href='/publications/'">show all publications</button>

## Selected talks

<div class="mt-4">
  {% assign talks_spotlight = site.talks | where: "spotlight", "yes" %}
  {% for talk in talks_spotlight %}
  {% assign idx_mod = forloop.index0 | modulo: 2 %}
  {% if idx_mod == 0 %}
  <div class="row" style="display: flex">
  {% endif %}
    {%- assign talk_venue = talk.venues[0] -%}
    <div class="col-sm-6 card-group">
      <div class="card">
        {%- if talk_venue.youtube -%}
        <div class="card-img-top">
          <iframe src="{{ talk_venue.youtube_embed }}" title="Embedded video for talk with title {{ talk.title }}" frameborder="0" allow="encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        {%- endif -%}
        <div class="card-body">
          <h3 class="card-title" style="margin: 0;">{{ talk.title }}</h3>
          <p class="page__meta fs-8">{{ talk_venue.name }}</p>
          {%- if talk.subtitle -%}
          <h6 class="card-subtitle mb-2 text-muted">{{ talk.subtitle }}</h6>
          {%- endif -%}
          {%- if talk.short_desc -%}
          <p class="card-text">{{ talk.short_desc }}</p>
          {%- endif -%}
          <a href="{{ base_path }}{{ talk.url }}" class="btn btn-link">More</a>
        </div>
      </div>
    </div>
  {% if idx_mod == 1 %}
  </div>
  {% endif %}
  {%- endfor %}
  {% if idx_mod == 0 %}
  </div>
  {% endif %}
  
  <button type="button" class="btn btn-link mt-2" onclick="window.location.href='/talks/'">show all talks</button>
</div>

## Selected Achievements

<ul>
{% for achievement in site.data.achievements %}
    {% if achievement.spotlight == 'yes' %}
        <li>{{ achievement.text | markdownify }}</li>
    {% endif %}
{% endfor %}
</ul>

<button type="button" class="btn btn-link" onclick="window.location.href='/cv/'">show CV</button>
