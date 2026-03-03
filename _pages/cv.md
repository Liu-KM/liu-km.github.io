---
layout: single
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

## Education

- **Ph.D. in Computer Science and Engineering**, The Hong Kong University of Science and Technology (HKUST), 2024 - Present
- **B.Sc. in Computing (First Class Honours), Minor in Applied Mathematics**, The Hong Kong Polytechnic University (PolyU), 2024

## Publications

{% for pub in site.data.publications %}
- **{{ pub.title }}**  
  {{ pub.authors }}  
  {% case pub.venue %}
    {% when "INFOCOM 2026" %}
      IEEE International Conference on Computer Communications (INFOCOM), 2026
    {% when "INFOCOM 2025" %}
      IEEE International Conference on Computer Communications (INFOCOM), 2025
    {% when "SIGMOD 2026" %}
      ACM SIGMOD/PODS International Conference on Management of Data (SIGMOD), 2026
    {% else %}
      {{ pub.venue }}
  {% endcase %}
  {% if pub.paper_url != "" %}  
  [Paper]({{ pub.paper_url }})
  {% endif %}
{% endfor %}

## Teaching Experience

{% for item in site.data.teaching %}
- **{{ item.course }}**, {{ item.role }}  
  {{ item.semester }}, {{ item.institution }}
{% endfor %}

## Awards

{% for award in site.data.awards %}
- **{{ award.title }}**, {{ award.date | date: "%Y-%m-%d" }}
{% endfor %}

## Academic Service

{% for service in site.data.academic_service %}
- **{{ service.role }}**, {{ service.title }} ({{ service.year }})
{% endfor %}
