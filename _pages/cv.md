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
* B.S. in Automation, Anhui University, 2013-2017
* M.S. in Control Science and Control Engineering, Southeast University, 2017-2020
* Ph.D in Control Science and Control Engineering, Zhejiang University, 2020-2024

Exchange
======
* 2023.02 - 2023.08:  Joint PhD student, ETH Zurich
  * ETH Zurich, Switzerland
  * Working on distributed adaptive minimax optimization in Optimization and Decision Intelligence (ODI) group
  * Supervisor: Niao He


Publications
======
  {% assign sorted_publications = site.publications | sort: "date" | reverse %}
  <ul>{% for post in sorted_publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
