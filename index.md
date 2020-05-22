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
<section class="section resume" id="resume">
  <h1>Resume</h1>
  <hr>
  <p>Section Under Development.</p>
</section>
<section class="section contact" id="contact">
  <h1>Contact</h1>
  <hr>
  {% include contact-form.html %}
</section>
<script>
window.addEventListener('scroll', updateArrow);
window.addEventListener('DOMContentLoaded', () => {
  let form = document.getElementById('contact-form');
  let submitButton = document.getElementById('contact-form-submit-button');
  let formStatus = document.getElementById('contact-form-status');

  form.addEventListener('submit', async (e) => {
    e.preventDefault();

    const action='https://formspree.io/mbjzdblw';
    const method='POST';

    let data = new FormData(form);

    try {
      const res = await makeRequest(method, action, data);
      form.reset();
      submitButton.disabled = true;
      formStatus.innerHTML = 'Email sent successfully!';
    } catch (err) {
      formStatus.innerHTML = 'Whoops! Something went wrong.';
    }
  });
});

function updateArrow() {
  let arrow = document.getElementById('landingArrow');
  if (window.scrollY !== 0) {
    arrow.style.opacity = '0';
    arrow.style.pointerEvents = 'none';
  }
  else {
    arrow.style.opacity = '1';
    arrow.style.pointerEvents = 'all';
  }
}

function makeRequest(method, url, data) {
  return new Promise(function (resolve, reject) {
    const xhr = new XMLHttpRequest();
    xhr.open(method, url);
    xhr.setRequestHeader("Accept", "application/json");
    xhr.onload = (e) => {
      console.log(this.status);
      if (xhr.status >= 200 && xhr.status < 300) {
        resolve(xhr.response);
      } else {
        reject({
          status: xhr.status,
          statusText: xhr.statusText
        });
      }
    };
    xhr.onerror = (e) => {
      reject({
        status: this.status,
        statusText: xhr.statusText
      });
    };
    xhr.send(data);
  });
}
</script>
