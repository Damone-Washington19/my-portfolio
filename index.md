---
layout: default
title: Home
---

<div class="hero">
  <img src="assets/images/MG_8539.jpeg" alt="Damone Washington" class="hero-photo">
  <div class="hero-text">
    <h2>Computer Science Student Building AI, Data, and Web Tools</h2>
    <p class="hero-tagline">Winston-Salem State University - NC-LSAMP Student Researcher - Google AI Certified</p>
    <p>I build practical software with Python, JavaScript, REST APIs, and graph-based data tools. I am seeking software engineering, full-stack web, and data operations internships where I can turn research-minded problem solving into reliable products.</p>
    <div class="hero-cta">
      <a href="#projects" class="cta-btn">View Projects</a>
      <a href="Damone_Washington.pdf" class="cta-btn">Download Resume</a>
      <a href="#contact" class="cta-btn cta-btn--outline">Contact Me</a>
    </div>
  </div>
</div>

---

## Recruiter Snapshot

<div class="snapshot-grid">
  <div class="snapshot-item">
    <strong>CS Student</strong>
    <span>Computer Science student at Winston-Salem State University with a 3.5 college GPA.</span>
  </div>
  <div class="snapshot-item">
    <strong>Research Experience</strong>
    <span>NC-LSAMP student researcher studying AI/ML security and adversarial computer vision risks.</span>
  </div>
  <div class="snapshot-item">
    <strong>Technical Builder</strong>
    <span>Built Python graph tools with NetworkX, BeautifulSoup, Matplotlib, JSON, and REST API workflows.</span>
  </div>
  <div class="snapshot-item">
    <strong>Career Target</strong>
    <span>Seeking software engineering, full-stack web development, and data operations internships.</span>
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
      <li>AI / ML Security</li>
      <li>Graph Theory</li>
      <li>NetworkX</li>
      <li>Matplotlib</li>
    </ul>
  </div>
  <div class="skill-category">
    <h4>Tools</h4>
    <ul>
      <li>Git / GitHub</li>
      <li>Jupyter Notebooks</li>
      <li>REST APIs</li>
      <li>BeautifulSoup</li>
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

## Research

<div class="research-list">
  <article class="research-item">
    <h3>Adversarial AI Defense Research</h3>
    <p>Studying physical adversarial patch attacks against computer vision object detection systems, with a focus on how real-world visual perturbations can affect AI model reliability.</p>
  </article>
  <article class="research-item">
    <h3>ADMI Symposium Presenter</h3>
    <p>Selected as a student presenter for ADMI Symposium research sessions in 2025 and 2026, presenting work connected to machine learning vulnerabilities and defensive AI thinking. <a href="https://ramswssuedu-my.sharepoint.com/:p:/r/personal/dwashington124_rams_wssu_edu/Documents/P1-JDRJ-Project%20PowerPoint.pptx?d=wf6877b2ec3a04edfb038fc79afbaef79&amp;csf=1&amp;web=1&amp;e=foO75E" target="_blank" rel="noopener">View presentation</a>.</p>
  </article>
  <article class="research-item">
    <h3>NC-LSAMP Student Researcher</h3>
    <p>Contributing to STEM research through NC-LSAMP while building stronger skills in technical communication, experimental thinking, and applied computer science.</p>
  </article>
</div>

---

<section id="projects">

## Projects

<div class="project-grid">
{% assign projects = site.projects | sort: "date" | reverse %}
{% for project in projects %}
  <div class="project-card">
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
    {% if project.tech %}<p class="project-tech">{{ project.tech | join: " &middot; " }}</p>{% endif %}
    <p>{{ project.content | strip_html | truncatewords: 30 }}</p>
    <div class="project-links">
      <a href="{{ project.url | relative_url }}">Read More &rarr;</a>
      {% if project.repo %}<a href="{{ project.repo }}" target="_blank" rel="noopener">Code &rarr;</a>{% endif %}
      {% if project.demo %}<a href="{{ project.demo }}" target="_blank" rel="noopener">Live Demo &rarr;</a>{% endif %}
    </div>
  </div>
{% endfor %}
</div>

</section>

---

## Currently Building

<div class="current-focus">
  <div>
    <strong>Backend utility automation</strong>
    <span>Python scripts, API workflows, file operations, and repeatable data processing tasks.</span>
  </div>
  <div>
    <strong>Full-stack web fundamentals</strong>
    <span>HTML, CSS, JavaScript, Jekyll, GitHub Pages, and portfolio-ready project documentation.</span>
  </div>
  <div>
    <strong>AI security research</strong>
    <span>Adversarial patch attacks, computer vision model reliability, and defensive ML thinking.</span>
  </div>
</div>

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
