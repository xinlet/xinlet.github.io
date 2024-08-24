---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D in Statistics, University of Bath, 2021-2025 (expected)
* M.Sc. in Statistics, The George Washington University, 2019-2021
* B.Sc. in Mathematics, University of British Columbia, 2015-2019

Skills
======
* R
* Python

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
