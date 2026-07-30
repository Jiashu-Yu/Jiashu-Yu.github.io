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

<div class="page-shell">
  <section class="profile-section" id="about" aria-labelledby="page-title">
    <div class="profile-row">
      <div class="profile-copy">
        <h1 class="name" id="page-title">Jiashu Yu</h1>
        <p>I am an undergraduate at <a href="https://www.xjc.tsinghua.edu.cn/" target="_blank" rel="noreferrer">Xingjian College, Tsinghua University</a>, pursuing a dual degree in Mechanics and Interdisciplinary Engineering. Currently, I am a visiting research student at <a href="https://ai4ce.github.io/" target="_blank" rel="noreferrer">NYU AI4CE Lab</a>, advised by <a href="https://engineering.nyu.edu/faculty/chen-feng" target="_blank" rel="noreferrer">Prof. Chen Feng</a>.</p>
        <p>My research interests center on learning-based approaches to robotics. At NYU, I work on dexterous manipulation and object navigation. Previously, at Tsinghua, I worked with <a href="https://designschool.sjtu.edu.cn/teacher/31104c124abec4f853ad19c8530ab586/viceprofessor/detail/69a8d4cfe67ee39d2475bd96" target="_blank" rel="noreferrer">Prof. Jiangtao Gong</a> on an LLM-based autonomous-driving evaluation framework.</p>
        <p class="contact-links">
          <a href="mailto:{{ site.author.email }}">Email</a>
          {% if site.author.googlescholar %}<span>/</span> <a href="{{ site.author.googlescholar }}" target="_blank" rel="noreferrer">Scholar</a>{% endif %}
          {% if site.author.github %}<span>/</span> <a href="https://github.com/{{ site.author.github }}" target="_blank" rel="noreferrer">Github</a>{% endif %}
          {% if site.author.linkedin %}<span>/</span> <a href="https://www.linkedin.com/in/{{ site.author.linkedin }}/" target="_blank" rel="noreferrer">Linkedin</a>{% endif %}
        </p>
      </div>

      <figure class="profile-photo-cell">
        <img class="profile-photo" src="{{ '/images/yjs-robot.jpg' | relative_url }}" alt="Jiashu Yu with a robot">
      </figure>
    </div>
  </section>

  <section class="site-section" id="news" aria-labelledby="news-title">
    <h2 id="news-title">Recent News</h2>
    <div class="news-panel">
      <div class="news-item">
        <time datetime="2026-03">2026.03</time>
        <span>Joined <a href="https://ai4ce.github.io/" target="_blank" rel="noreferrer"><strong>NYU AI4CE</strong></a> as a visiting research student.</span>
      </div>
      <div class="news-item">
        <time datetime="2025-01">2025.01</time>
        <span><a href="https://jiashu-yu.github.io/files/A_Comprehensive_LLM-powered_Framework_for_Driving_Intelligence_Evaluation.pdf"><strong>A Comprehensive LLM-Powered Framework for Driving Intelligence Evaluation</strong></a> was accepted to <strong>ICRA 2025</strong>.</span>
      </div>
    </div>
  </section>

  <section class="site-section" id="experience" aria-labelledby="experience-title">
    <h2 id="experience-title">Research Experience</h2>
    <div class="timeline-list">
      <div class="timeline-item pending-row">To be added.</div>
    </div>
  </section>

  <section class="site-section" id="education" aria-labelledby="education-title">
    <h2 id="education-title">Education</h2>
    <div class="timeline-list">
      <div class="education-item">
        <div class="education-details">
          <a class="education-school" href="https://www.tsinghua.edu.cn/en/" target="_blank" rel="noreferrer">Tsinghua University</a>
          <div class="education-program">B.Sc. in Mechanics &amp; B.Eng. in Interdisciplinary Engineering, <a href="https://www.xjc.tsinghua.edu.cn/" target="_blank" rel="noreferrer">Xingjian College</a></div>
        </div>
        <time datetime="2022">2022 - Present</time>
      </div>
    </div>
  </section>

  <section class="site-section" id="research" aria-labelledby="research-title">
    <h2 id="research-title">Research</h2>
    <div class="publication-list">
      {% assign publications = site.publications | sort: 'date' | reverse %}
      {% for post in publications %}
        <article class="paper-row{% if post.paperurl contains 'A_Comprehensive_LLM-powered_Framework' %} paper-row--with-media{% endif %}">
          {% if post.paperurl contains 'A_Comprehensive_LLM-powered_Framework' %}
            <a class="paper-figure" href="{{ post.paperurl }}" target="_blank" rel="noreferrer">
              <img src="{{ '/images/research/icra-2025-evaluation-framework.png' | relative_url }}" alt="Architecture of the LLM-powered driving intelligence evaluation framework">
            </a>
          {% endif %}
          <div class="paper-content">
            {% if post.paperurl %}
              <a class="paper-title" href="{{ post.paperurl }}" target="_blank" rel="noreferrer">{{ post.title }}</a>
            {% else %}
              <a class="paper-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
            {% endif %}
            <div class="paper-authors">{{ post.authors | markdownify | remove: '<p>' | remove: '</p>' }}</div>
            <div class="paper-venue">{{ post.venue }}, {{ post.date | date: '%Y' }}</div>
            <div class="paper-links">
              {% if post.paperurl %}<a href="{{ post.paperurl }}" target="_blank" rel="noreferrer">paper</a>{% endif %}
              {% if site.author.googlescholar %}<span>/</span> <a href="{{ site.author.googlescholar }}" target="_blank" rel="noreferrer">scholar</a>{% endif %}
            </div>
            <div class="paper-summary">{{ post.content }}</div>
          </div>
        </article>
      {% endfor %}
    </div>
  </section>

  <section class="site-section" id="honors" aria-labelledby="honors-title">
    <h2 id="honors-title">Honors &amp; Awards</h2>
    <div class="timeline-list">
      <div class="award-item">
        <time datetime="2025-11">2025.11</time>
        <span>Science and Technology Innovation Excellence Scholarship, Tsinghua University</span>
      </div>
      <div class="award-item">
        <time datetime="2024-12">2024.12</time>
        <span>Academic Excellence Scholarship, Tsinghua University</span>
      </div>
    </div>
  </section>
</div>
