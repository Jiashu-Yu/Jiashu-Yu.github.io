---
permalink: /
title: "Jiashu Yu"
description: "Jiashu Yu — robotics and robot learning."
layout: research-home
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

<div class="shell page-stack">
  <section class="profile-panel" id="about" aria-labelledby="page-title">
    <div class="profile-copy">
      <p class="profile-kicker">Robotics · Robot Learning</p>
      <h1 id="page-title">Jiashu Yu</h1>

      <div class="profile-intro">
        <p>I am an undergraduate at <a href="https://www.xjc.tsinghua.edu.cn/" target="_blank" rel="noreferrer">Xingjian College, Tsinghua University</a>, pursuing a dual degree in Mechanics and Interdisciplinary Engineering. Currently, I am a visiting research student at <a href="https://ai4ce.github.io/" target="_blank" rel="noreferrer">NYU AI4CE Lab</a>, advised by <a href="https://engineering.nyu.edu/faculty/chen-feng" target="_blank" rel="noreferrer">Prof. Chen Feng</a>.</p>
        <p>My research interests are in robotics and robot learning. At NYU, I currently work on object reorientation from human demonstrations, following earlier work on object-goal navigation. Previously, at Tsinghua, I worked with <a href="https://designschool.sjtu.edu.cn/teacher/31104c124abec4f853ad19c8530ab586/viceprofessor/detail/69a8d4cfe67ee39d2475bd96" target="_blank" rel="noreferrer">Prof. Jiangtao Gong</a> on LLM/VLM-based autonomous-driving systems.</p>
      </div>

      <div class="profile-links" aria-label="Profile links">
        <a href="mailto:{{ site.author.email }}">Email</a>
        {% if site.author.googlescholar %}<a href="{{ site.author.googlescholar }}" target="_blank" rel="noreferrer">Scholar</a>{% endif %}
        {% if site.author.github %}<a href="https://github.com/{{ site.author.github }}" target="_blank" rel="noreferrer">GitHub</a>{% endif %}
        {% if site.author.linkedin %}<a href="https://www.linkedin.com/in/{{ site.author.linkedin }}/" target="_blank" rel="noreferrer">LinkedIn</a>{% endif %}
      </div>
    </div>

    <figure class="portrait-wrap">
      <img class="portrait" src="{{ '/images/yjs.jpg' | relative_url }}" alt="Portrait of Jiashu Yu">
    </figure>
  </section>

  <section class="content-section" id="news" aria-labelledby="news-title">
    <div class="section-heading">
      <p>01 / Updates</p>
      <h2 id="news-title">Recent News</h2>
    </div>
    <div class="section-placeholder news-placeholder">
      <span>Next</span>
      <p>News items will be added after the layout is finalized.</p>
    </div>
  </section>

  <div class="split-sections">
    <section class="content-section" id="experience" aria-labelledby="experience-title">
      <div class="section-heading">
        <p>02 / Timeline</p>
        <h2 id="experience-title">Research Experience</h2>
      </div>
      <div class="section-placeholder">
        <span>To add</span>
        <p>Roles, affiliations, dates, and advisors.</p>
      </div>
    </section>

    <section class="content-section" id="education" aria-labelledby="education-title">
      <div class="section-heading">
        <p>03 / Background</p>
        <h2 id="education-title">Education</h2>
      </div>
      <div class="section-placeholder">
        <span>To add</span>
        <p>Degrees, programs, and academic milestones.</p>
      </div>
    </section>
  </div>

  <section class="content-section" id="research" aria-labelledby="research-title">
    <div class="section-heading">
      <p>04 / Selected Work</p>
      <h2 id="research-title">Research</h2>
    </div>

    <div class="research-list">
      {% assign publications = site.publications | sort: 'date' | reverse %}
      {% for post in publications %}
        <article class="research-card">
          <div class="research-year" aria-hidden="true">{{ post.date | date: '%Y' }}</div>
          <div class="research-copy">
            <p class="publication-meta">{{ post.venue }}</p>
            {% if post.paperurl %}
              <h3><a href="{{ post.paperurl }}" target="_blank" rel="noreferrer">{{ post.title }}</a></h3>
            {% else %}
              <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            {% endif %}
            <p class="publication-authors">{{ post.authors | markdownify | remove: '<p>' | remove: '</p>' }}</p>
            <div class="publication-summary">{{ post.content }}</div>
            <div class="publication-links">
              {% if post.paperurl %}<a href="{{ post.paperurl }}" target="_blank" rel="noreferrer">Paper</a>{% endif %}
              {% if site.author.googlescholar %}<a href="{{ site.author.googlescholar }}" target="_blank" rel="noreferrer">Scholar</a>{% endif %}
            </div>
          </div>
        </article>
      {% endfor %}
    </div>
  </section>

  <section class="content-section" id="honors" aria-labelledby="honors-title">
    <div class="section-heading">
      <p>05 / Recognition</p>
      <h2 id="honors-title">Honors &amp; Awards</h2>
    </div>
    <div class="section-placeholder">
      <span>To add</span>
      <p>Tsinghua University awards and other selected honors.</p>
    </div>
  </section>
</div>
