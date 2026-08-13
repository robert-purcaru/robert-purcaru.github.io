---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<!--
  TODO: drop your PDF at /files/cv.pdf and uncomment the line below.
  <p><a href="{{ base_path }}/files/cv.pdf">Download as PDF</a></p>
-->

Education
======

See the [Education](/education/) page for full detail.

* TODO: Ph.D. in Field, Institution, Year
* TODO: M.Sc. in Field, Institution, Year
* TODO: B.Sc. in Field, Institution, Year

Experience
======

* **TODO: Year–Year — Job title**, Organisation
  * TODO: what you did, one line each
  * TODO: second line

* **TODO: Year–Year — Job title**, Organisation
  * TODO: what you did

Skills
======

* TODO: skill area
  * TODO: specifics
* TODO: skill area
* TODO: languages spoken

Publications
======

  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Projects
======

  <ul>{% for post in site.projects reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Service and outreach
======

* TODO: reviewing, committees, mentoring, volunteering
