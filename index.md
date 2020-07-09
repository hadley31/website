---
title: Homepage
layout: default
image: /assets/images/headshot.png
---

<section class="section landing" id="home">
  <div class="landing-name">Nicholas Hadley</div>
  <div class="landing-position">Full Stack Software Developer</div>
  <a href="#about" id="landingArrow"></a>
</section>
<section class="section about" id="about">
  <img class="portrait" src="{{ '/assets/images/headshot.png' | relative_url }}" />
  <p>Hello! My name is Nicholas Hadley and I am a Full Stack Software Developer from Savannah, Georgia. I am currently pursuing my Bachelor's Degree at Georgia Southern University.</p>
</section>
<section class="section portfolio" id="portfolio">
  <h1>Projects</h1>
  <hr>
  {% include project-list.html projects=site.projects %}
</section>
<section class="section resume" id="resume">
  <h1>Resume</h1>
  <hr>
  <p>Interactive Section in the Works!</p>
</section>
<section class="section contact" id="contact">
  <h1>Contact</h1>
  <hr>
  {% include contact-form.html %}
</section>
<script defer>
window.addEventListener('scroll', () => {
  const arrow = document.getElementById('landingArrow');
  if (window.scrollY !== 0) {
    arrow.style.opacity = '0';
    arrow.style.pointerEvents = 'none';
  }
  else {
    arrow.style.opacity = '1';
    arrow.style.pointerEvents = 'all';
  }
});
</script>
