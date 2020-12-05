---
title: Homepage
layout: default
image: /assets/images/headshot.png
description: Hello! My name is Nicholas Hadley and I am a Full Stack Software Developer from Savannah, Georgia. I am currently pursuing my Bachelor's Degree at Georgia Southern University in Computer Science.
---

<!-- Landing Section -->

<section class="section landing sticky" id="home">
  <div class="landing-name">Nicholas Hadley</div>
  <div class="landing-position">Full Stack Software Developer</div>
  <a href="#about" id="landingArrow"></a>
</section>

<!-- About Summary -->

<section class="section about sticky" id="about">
  <img class="portrait" src="{{ '/assets/images/headshot.png' | relative_url }}" />
  <p>Hello! My name is Nicholas Hadley and I am a Full Stack Software Developer from Savannah, Georgia. I am currently pursuing my Bachelor's Degree at Georgia Southern University in Computer Science.</p>
</section>

<!-- Projects -->

<section class="section portfolio not-sticky" id="portfolio">
  <h1>Projects</h1>
  <hr>
  {% include project-list.html projects=site.projects %}
</section>

<!-- Resume -->

<section class="section resume not-sticky" id="resume">
  <h1>Resume</h1>
  <hr>
  <p>Interactive Section in the Works!</p>
  <a class="button" href="{{ '/assets/resume.pdf' | relative_url }}">Download</a>
</section>

<!-- Contact -->

<section class="section contact not-sticky" id="contact">
  <h1>Contact</h1>
  <hr>
  {% include contact-form.html %}
</section>

<!-- Landing Section Arrow Script -->

<script defer>
  const arrow = document.getElementById('landingArrow');
  window.addEventListener('scroll', () => {
    arrow.classList.toggle("hidden", window.scrollY !== 0);
  });
</script>
