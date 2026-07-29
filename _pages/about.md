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
    <p class="eyebrow">Embodied AI · Robot Learning · Navigation &amp; Manipulation</p>
    <h1 id="page-title">Jiashu <span>Yu</span></h1>

    <div class="hero-intro">
      <p>I am an undergraduate at <a href="https://www.xjc.tsinghua.edu.cn/" target="_blank" rel="noreferrer">Xingjian College, Tsinghua University</a>, pursuing a dual degree in Mechanics and Interdisciplinary Engineering. Currently, I am a visiting research student at <a href="https://ai4ce.github.io/" target="_blank" rel="noreferrer">NYU AI4CE Lab</a>, advised by <a href="https://engineering.nyu.edu/faculty/chen-feng" target="_blank" rel="noreferrer">Prof. Chen Feng</a>.</p>
      <p>My research interests lie in embodied AI and robot learning, particularly visual navigation and dexterous manipulation. At NYU, I have worked on object-goal navigation and am currently studying contact-rich object reorientation from human hand–object demonstrations. Previously, at Tsinghua University's Institute for AI Industry Research, I worked with <a href="https://designschool.sjtu.edu.cn/teacher/31104c124abec4f853ad19c8530ab586/viceprofessor/detail/69a8d4cfe67ee39d2475bd96" target="_blank" rel="noreferrer">Prof. Jiangtao Gong</a>—now an Associate Professor at Shanghai Jiao Tong University—on LLM/VLM-based autonomous-driving systems.</p>
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
  </figure>
</section>

<section class="section" id="publications" aria-labelledby="publications-title">
  <div class="shell">
    <div class="section-heading">
      <div>
        <p class="eyebrow">Research</p>
        <h2 id="publications-title">Publications</h2>
      </div>
    </div>

    <div class="publication-list">
      {% assign publications = site.publications | sort: 'date' | reverse %}
      {% for post in publications %}
        <article class="publication">
          <div class="publication-index" aria-hidden="true">{% if forloop.index < 10 %}0{% endif %}{{ forloop.index }}</div>
          <div>
            <p class="publication-meta">{{ post.venue }} · {{ post.date | date: '%Y' }}</p>
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
  </div>
</section>
