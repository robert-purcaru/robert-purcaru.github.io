---
permalink: /
author_profile: true
---

{% comment %}
  The whole site is this one scrolling page. Each <section> id matches a nav
  link in _data/navigation.yml. Content lives in:
    Education / Industry rows  -> _data/experience.yml
    Publications               -> _publications/
    Projects                   -> _projects/
{% endcomment %}

<section id="about" class="home-section" markdown="1">
<h2 class="section-title">About</h2>

I'm an MSc student in Computational Science and Engineering at ETH Zürich,
Specialization: robotics. Before that I was a quantitative analyst at
Squarepoint Capital, and I studied Engineering Science at the University of
Toronto, where I worked on balloon-borne telescopes, numerical optimization, and embedded
hardware.

<h3 class="subsection-title">Education</h3>
<div class="xp-list">
{% for item in site.data.experience.education %}{% include experience-row.html item=item %}{% endfor %}
</div>
</section>

<section id="publications" class="home-section">
<h2 class="section-title">Publications</h2>
{% include publication-list.html %}
</section>

<section id="industry" class="home-section">
<h2 class="section-title">Industry Experience</h2>
<div class="xp-list">
{% for item in site.data.experience.industry %}{% include experience-row.html item=item %}{% endfor %}
</div>
</section>

<section id="projects" class="home-section">
<h2 class="section-title">Projects</h2>
{% include project-list.html section="projects" %}
</section>
