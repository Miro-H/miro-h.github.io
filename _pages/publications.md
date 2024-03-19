---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

**Publications are sorted in reverse order of publication. Stars (\*) mark the first author(s).**

{% include base_path %}

## Papers

{% for post in site.papers reversed %}
  {% include archive-publication.html %}
{% endfor %}

## Articles

{% for post in site.articles reversed %}
  {% include archive-publication.html %}
{% endfor %}

