---
permalink: /
title: "Jiashu Yu"
description: "Jiashu Yu — robotics, reinforcement learning, and embodied AI."
layout: research-home
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

<section class="shell hero" id="about" aria-labelledby="page-title">
  <div>
    <p class="eyebrow">Robotics · Reinforcement Learning · Embodied AI</p>
    <h1 id="page-title">Jiashu <span>Yu</span></h1>

    <div class="hero-intro">
      <p>I am an undergraduate at <a href="https://www.xjc.tsinghua.edu.cn/" target="_blank" rel="noreferrer">Xingjian College, Tsinghua University</a>, pursuing a dual degree in Mechanics and Interdisciplinary Engineering. Currently, I am a visiting research student at <a href="https://ai4ce.github.io/" target="_blank" rel="noreferrer">NYU AI4CE Lab</a>, advised by <a href="https://engineering.nyu.edu/faculty/chen-feng" target="_blank" rel="noreferrer">Prof. Chen Feng</a>.</p>
      <p>I work on learning-based methods for embodied intelligence. Previously, I worked with <a href="https://air.tsinghua.edu.cn/en/info/1046/1188.htm" target="_blank" rel="noreferrer">Prof. Jiangtao Gong</a> at Tsinghua University's Institute for AI Industry Research on LLM/VLM-based autonomous-driving systems. My broader interests include robotics, reinforcement learning, and vision-language-action models.</p>
    </div>

    <div class="profile-links" aria-label="Profile links">
      <a href="mailto:{{ site.author.email }}">Email</a>
      {% if site.author.googlescholar %}<a href="{{ site.author.googlescholar }}" target="_blank" rel="noreferrer">Google Scholar</a>{% endif %}
      {% if site.author.github %}<a href="https://github.com/{{ site.author.github }}" target="_blank" rel="noreferrer">GitHub</a>{% endif %}
      {% if site.author.linkedin %}<a href="https://www.linkedin.com/in/{{ site.author.linkedin }}/" target="_blank" rel="noreferrer">LinkedIn</a>{% endif %}
    </div>
  </div>

  <figure class="portrait-wrap">
    <img class="portrait" src="{{ '/images/yjs.jpg' | relative_url }}" alt="Portrait of Jiashu Yu">
    <figcaption class="portrait-caption">NYU AI4CE · Summer 2026</figcaption>
  </figure>
</section>

<section class="section" id="publications" aria-labelledby="publications-title">
  <div class="shell">
    <div class="section-heading">
      <div>
        <p class="eyebrow">Research</p>
        <h2 id="publications-title">Publications</h2>
      </div>
      <p>Work on intelligent systems that connect perception, reasoning, and action. Publication metadata and links are rendered directly from the existing collection.</p>
    </div>

    <div class="publication-list">
      {% assign publications = site.publications | sort: 'date' | reverse %}
      {% for post in publications %}
        {% assign publication_url = post.paperurl | default: post.url %}
        <article class="publication">
          <div class="publication-index" aria-hidden="true">{% if forloop.index < 10 %}0{% endif %}{{ forloop.index }}</div>
          <div>
            <p class="publication-meta">{{ post.venue }} · {{ post.date | date: '%Y' }}</p>
            <h3><a href="{{ publication_url | relative_url }}"{% if post.paperurl %} target="_blank" rel="noreferrer"{% endif %}>{{ post.title }}</a></h3>
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
  </div>
</section>
