---
title: Homepage
layout: default
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
  <h1 class="text-center">Projects</h1>
  <hr>
  {% include project-list.html projects=site.projects %}
</section>
<section class="section resume text-center" id="resume">
  <h1>Resume</h1>
  <hr>
  <p>Section Under Development.</p>
</section>
<script>
  window.onscroll = updateArrow;
  function updateArrow() {
    let arrow = document.getElementById('landingArrow');
    if (window.scrollY !== 0){
      arrow.style.opacity = "0";
      arrow.style.display = "none";
    }
    else{
      arrow.style.opacity = "1";
      arrow.style.display = "inline";
    }
  }
</script>
