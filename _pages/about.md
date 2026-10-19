---
permalink: /
title: "LIU Qianli's Homepage"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
/* 直接在页面内定义样式 */
.publication {
  margin-bottom: 2rem !important;
}

.pub-item {
  position: relative;
  margin-bottom: 1.1rem;
  padding-left: 1.65rem;
  line-height: 1.45;
}

.pub-number {
  position: absolute;
  left: 0;
  top: 0.1rem;
  color: #666;
  font-size: 0.85rem;
}

.pub-title {
  font-weight: 700;
  font-size: 1rem;
  margin-bottom: 0.2rem;
  color: #2a2a2a;
}

.pub-title a,
.pub-title a:visited,
.pub-title a:hover,
.pub-title a:focus {
  color: inherit;
  text-decoration: none;
}

.pub-title a:hover,
.pub-title a:focus-visible {
  text-decoration: underline;
  text-underline-offset: 0.15em;
}

.pub-authors {
  margin-bottom: 0.15rem;
  font-size: 0.85rem;
  color: #3a3a3a;
}

.pub-venue {
  font-size: 0.85rem;
  font-style: italic;
  color: #555;
}

.venue-abbr {
  font-style: normal;
  color: #777;
}

.pub-code {
  margin-left: 0.4rem;
  font-style: normal;
}

.award-item {
  display: flex !important;
  justify-content: space-between !important;
  margin-bottom: 0.8rem !important;
  padding-left: 0.5rem !important;
  border-left: 2px solid #f0ad4e !important;
}

.award-title {
  font-weight: bold !important;
  color: #333 !important;
}

.award-date {
  color: #777 !important;
  font-style: italic !important;
}

/* 修改新闻项的样式 */
.news-container {
  margin-bottom: 2rem !important;
  max-height: 16rem;
  overflow-y: auto;
  padding-right: 0.75rem;
  scrollbar-gutter: stable;
}

.news-container:focus-visible {
  outline: 2px solid #2a76dd;
  outline-offset: 4px;
}

.news-item {
  position: relative !important;
  margin-bottom: 0.8rem !important;
  display: flex !important;
}

.news-date {
  font-size: 1rem !important;
  font-weight: normal !important;
  /* color: black !important; */
  margin-right: 0.5rem !important;
  /* font-family: "Menlo","Liberation Mono", monospace !important; */
  min-width: 6rem !important;
  display: inline-block !important;
}

.news-content {
  display: inline !important;
  flex: 1 !important;
}

/* 教学经历的样式 */
.teaching-container {
  margin-bottom: 2rem !important;
}

.teaching-item {
  margin-bottom: 1rem !important;
  padding-left: 0.5rem !important;
  border-left: 2px solid #4a86e8 !important;
}

.teaching-course {
  font-weight: bold !important;
  color: #333 !important;
  margin-bottom: 0.3rem !important;
}

.teaching-role {
  display: inline-block !important;
  margin-left: 0.5rem !important;
}

.teaching-info {
  color: #777 !important;
  font-style: italic !important;
}

/* 学术服务的样式 */
.service-container {
  margin-bottom: 2rem !important;
}

.service-item {
  margin-bottom: 1rem !important;
  padding-left: 0.5rem !important;
  border-left: 2px solid #5cb85c !important;
}

.service-title {
  font-weight: bold !important;
  color: #333 !important;
  margin-bottom: 0.3rem !important;
}

.service-info {
  color: #777 !important;
  font-style: italic !important;
}

.presentation-container {
  margin-bottom: 2rem !important;
}

.presentation-item {
  margin-bottom: 1rem !important;
  padding-left: 0.5rem !important;
  border-left: 2px solid #a06cd5 !important;
}

.presentation-title {
  font-weight: bold !important;
  color: #333 !important;
  margin-bottom: 0.3rem !important;
}

.presentation-info {
  color: #777 !important;
  font-style: italic !important;
}

.leadership-container {
  margin-bottom: 2rem !important;
}

.leadership-item {
  margin-bottom: 1rem !important;
  padding-left: 0.5rem !important;
  border-left: 2px solid #e67e22 !important;
}

.leadership-title {
  font-weight: bold !important;
  color: #333 !important;
  margin-bottom: 0.3rem !important;
}

.leadership-info {
  color: #777 !important;
  font-style: italic !important;
}

</style>

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
