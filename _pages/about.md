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
    <p>{{ author.bio | default: "Add a short bio here. A few sentences on your research interests, methods, and current affiliation usually work well." }}</p>
  </div>
</div>

<section class="home-section">
  <p class="home-section__label">Work in Progress</p>
  <p>Use this section for current projects, draft papers, and ongoing collaborations. A short paragraph on each project or a concise list of working papers works well here.</p>
</section>
