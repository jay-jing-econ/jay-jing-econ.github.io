---
permalink: /
layout: home
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}
{% assign author = site.author %}

<div class="home-intro">
  <div class="home-intro__summary">
    <div class="home-intro__photo">
      {% if author.avatar contains "://" %}
        <img src="{{ author.avatar }}" alt="{{ site.title }}" fetchpriority="high">
      {% else %}
        <img src="{{ author.avatar | prepend: '/images/' | prepend: base_path }}" alt="{{ site.title }}" fetchpriority="high">
      {% endif %}
    </div>

    <div class="home-intro__identity">
      <h1 class="home-intro__name">{{ site.title }}</h1>
      <ul class="home-intro__details">
        {% if author.email %}
          <li><span>Email</span><a href="mailto:{{ author.email }}">{{ author.email }}</a></li>
        {% endif %}
        {% if author.employer %}
          <li><span>University</span>{{ author.employer }}</li>
        {% endif %}
      </ul>
    </div>
  </div>

  <div class="home-intro__bio">
    <p class="home-section__label">Short Bio</p>
    {{ author.bio | markdownify }}
  </div>
</div>

<section class="home-section">
  <p class="home-section__label">Work in Progress</p>
  <div class="home-project">
    <h3 class="home-project__title">Project Title Placeholder 1</h3>
    <p>Abstract placeholder for work-in-progress project 1. Add a short summary of the research question, approach, and current status here.</p>
  </div>

  <div class="home-project">
    <h3 class="home-project__title">Project Title Placeholder 2</h3>
    <p>Abstract placeholder for work-in-progress project 2. Add a short summary of the research question, approach, and current status here.</p>
  </div>
</section>
