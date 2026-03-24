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
    <h3 class="home-project__title">Cyberattack and the Rise of the Cyberstate <em>(with <a href="https://www.juanfeliperiano.com" target="_blank" rel="noopener noreferrer">Juan Felipe Riaño</a>)</em></h3>
    <p> From tax filing to emergency information, many core government services now depend on websites that can be disrupted by cyberattacks. This project provides the first causal evidence that DDoS attacks reduce the reliability of these services using novel high-frequency data. We further investigate how governments respond by reshaping their digital infrastructure, pointing to the emergence of a “cyberstate”. </p>
  </div>

  <div class="home-project">
    <h3 class="home-project__title">Government Downsizing and Performance </h3>
    <p> In 2025, around 350,000 federal government employees were laid off during the mass layoffs to increase government efficiency. However, little is known about the consequences of these workforce reductions. This project studies how such government downsizing affects worker performance. </p>
  </div>
</section>
