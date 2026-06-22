---
layout: default
title: Home
---

<div class="hero">
  <img src="{{ '/assets/images/MG_8539-1.jpeg' | relative_url }}" alt="Damone Washington" class="hero-photo">
  <div class="hero-text">
    <h2>AI Researcher &amp; Software Developer</h2>
    <p class="hero-tagline">Rising Senior · Winston-Salem State University · NC-LSAMP Student Researcher · Google AI Certified</p>
    <p>I build intelligent systems and data-driven tools — from knowledge graphs and web crawlers to AI-powered applications. I'm driven by curiosity and committed to writing software that solves real-world problems.</p>
    <div class="hero-cta">
      <a href="#projects" class="cta-btn">View Projects</a>
      <a href="#contact" class="cta-btn cta-btn--outline">Contact Me</a>
    </div>
  </div>
</div>

---

## Skills

<div class="skills-grid">
  <div class="skill-category">
    <h4>Languages</h4>
    <ul>
      <li>Python</li>
      <li>Java</li>
      <li>HTML / CSS</li>
      <li>JavaScript</li>
    </ul>
  </div>
  <div class="skill-category">
    <h4>AI &amp; Data</h4>
    <ul>
      <li>Artificial Intelligence</li>
      <li>NetworkX</li>
      <li>Matplotlib</li>
      <li>BeautifulSoup</li>
    </ul>
  </div>
  <div class="skill-category">
    <h4>Tools</h4>
    <ul>
      <li>Git / GitHub</li>
      <li>Jupyter Notebooks</li>
      <li>REST APIs</li>
      <li>Jekyll</li>
    </ul>
  </div>
  <div class="skill-category">
    <h4>Certifications</h4>
    <ul>
      <li>Google AI</li>
    </ul>
  </div>
</div>

---

<section id="projects">

## Projects

<div class="project-grid">
{% for project in site.projects %}
  <div class="project-card">
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
    {% if project.tech %}<p class="project-tech">{{ project.tech | join: " &middot; " }}</p>{% endif %}
    <p>{{ project.content | strip_html | truncatewords: 30 }}</p>
    <div class="project-links">
      {% if project.repo %}<a href="{{ project.repo }}" target="_blank" rel="noopener">Code &rarr;</a>{% endif %}
      {% if project.demo %}<a href="{{ project.demo }}" target="_blank" rel="noopener">Live Demo &rarr;</a>{% endif %}
    </div>
  </div>
{% endfor %}
</div>

</section>

---

<section id="contact">

## Contact

<div class="contact-section">
  <p>I'm actively seeking internship opportunities in software engineering, AI, and data science. Let's connect.</p>
  <div class="contact-links">
    <a href="mailto:dwashington124@rams.wssu.edu" class="contact-link">dwashington124@rams.wssu.edu</a>
    <a href="https://www.linkedin.com/in/damone-washington-548765325/" target="_blank" rel="noopener" class="contact-link">LinkedIn</a>
    <a href="https://github.com/Damone-Washington19" target="_blank" rel="noopener" class="contact-link">GitHub</a>
  </div>
</div>

</section>
