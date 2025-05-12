---
title: Homepage
layout: default
image: /assets/images/headshot.png
description: Hello! My name is Nicholas Hadley and I am a Full Stack Software Developer from Savannah, Georgia. I got my Bachelor's Degree at Georgia Southern University in Computer Science.
---

<!-- Landing Section -->

<section class="section landing" id="home">
  <div class="landing-name">Nicholas Hadley</div>
  <div class="landing-position">Full Stack Software Developer</div>
  <a href="#about" id="landingArrow"></a>
</section>

<!-- About Summary -->

<section class="section about" id="about">
  <img class="portrait" src="{{ '/assets/images/headshot.png' | relative_url }}" />
  <p>Hello! My name is Nicholas Hadley and I am a Full Stack Software Developer currently residing in Atlanta, GA. In the past, I have worked for General Dynamics Mission Systems, and currently work for Capital One. I enjoy using technologies like Python, Node.js, C#, Vue.js, Flutter, Unity, and many more. Check out some of my projects below. Thanks for stopping by!</p>
</section>

<!-- Projects -->

<section class="section portfolio" id="portfolio">
  <h1>Projects</h1>
  <hr>
  {% include project-list.html projects=site.projects %}
</section>

<!-- Resume -->

<section class="section resume" id="resume">
  <h1>Resume</h1>
  <hr>
  <a class="button" href="{{ '/assets/resume.pdf' | relative_url }}">Download</a>
</section>

<!-- Contact -->

<section class="section contact" id="contact">
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
