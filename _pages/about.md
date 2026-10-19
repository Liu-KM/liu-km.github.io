---
permalink: /
title: "LIU Qianli's Homepage"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hey, this is Qianli. I am a third-year Ph.D. candidate at the [PEI Lab](https://peilab.netlify.app/) of the Hong Kong University of Science and Technology (HKUST), advised by Prof. Song Guo. My research focuses on efficient and scalable foundation model serving, with a particular interest in stateful AI systems, inference-state management, distributed MoE serving, and KV-cache management. Prior to HKUST, I received my B.Sc. in Computing with a minor in Applied Mathematics from the Hong Kong Polytechnic University (PolyU).

## 🔥 News
<div class="news-container" role="region" aria-label="News" tabindex="0">
{% for item in site.data.news %}
<div class="news-item">
  <span class="news-date">[{{ item.date }}]</span>
  <span class="news-content">{{ item.content | replace: "Prof. Song Guo", "<strong>Prof. Song Guo</strong>"  }}</span>
</div>
{% endfor %}
</div>

## 📃 Publication
<div class="publication">
{% for pub in site.data.publications %}
  <div class="pub-item">
    <div class="pub-number">[{{ forloop.index }}]</div>
    <div class="pub-title">{% if pub.paper_url and pub.paper_url != "" %}<a href="{{ pub.paper_url }}">{{ pub.title }}</a>{% else %}{{ pub.title }}{% endif %}</div>
    <div class="pub-authors">{{ pub.authors | replace: "Qianli Liu", "<strong>Qianli Liu</strong>" }}</div>
    <div class="pub-venue">
      {% case pub.venue %}
        {% when "INFOCOM 2026" %}
          IEEE International Conference on Computer Communications <span class="venue-abbr">(INFOCOM)</span>, 2026
        {% when "INFOCOM 2025" %}
          IEEE International Conference on Computer Communications <span class="venue-abbr">(INFOCOM)</span>, 2025
        {% when "SIGMOD 2026" %}
          ACM SIGMOD/PODS International Conference on Management of Data <span class="venue-abbr">(SIGMOD)</span>, 2026
        {% else %}
          {{ pub.venue }}
      {% endcase %}
      {% if pub.code_url and pub.code_url != "" %}
      <a class="pub-code" href="{{ pub.code_url }}">[Code]</a>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>


## 👨‍🏫 Teaching Experience
<div class="teaching-container">
{% for item in site.data.teaching %}
  <div class="teaching-item">
    <div class="teaching-course">
      {{ item.course }}{% if item.role %}<span class="teaching-role">({{ item.role }})</span>{% endif %}
    </div>
    <div class="teaching-info">{{ item.semester }} · {{ item.institution }}</div>
  </div>
{% endfor %}
</div>

## 🏅 Award
<div class="awards-container">
{% for award in site.data.awards %}
  <div class="award-item">
    <span class="award-title">{{ award.title }}</span>
    <span class="award-date">{{ award.date | date: "%Y.%m.%d" }}</span>
  </div>
{% endfor %}
</div>
## 🎓 Academic Service
<div class="service-container">
{% for service in site.data.academic_service %}
  <div class="service-item">
    <div class="service-title">{{ service.title }}</div>
    <div class="service-info">{{ service.role }} · {{ service.year }}</div>
  </div>
{% endfor %}
</div>


## 🎤 Presentations
<div class="presentation-container">
{% for item in site.data.presentations %}
  <div class="presentation-item">
    <div class="presentation-title">{{ item.title }}</div>
    <div class="presentation-info">{{ item.type }} · {{ item.location }} · {{ item.date }}</div>
  </div>
{% endfor %}
</div>

## 🤝 Leadership & Activities
<div class="leadership-container">
{% for item in site.data.leadership %}
  <div class="leadership-item">
    <div class="leadership-title">{{ item.role }} · {{ item.organization }}</div>
    <div class="leadership-info">{{ item.period }}</div>
    <div>{{ item.description }}</div>
  </div>
{% endfor %}
</div>
