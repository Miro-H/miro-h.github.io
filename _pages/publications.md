---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

**Papers are sorted in reverse order of publication. Stars (\*) mark the first author(s).**


{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-publication.html %}
{% endfor %}
