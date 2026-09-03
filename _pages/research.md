---
layout: archive
title: "Research & Paper Reviews"
permalink: /research/
author_profile: true
---

{% include base_path %}

Critical evaluations, methodology breakdowns, and technical deconstructions of academic literature across Systems and AI Security.

---

<style>
.post-card {
  border: 1px solid rgba(128, 128, 128, 0.3);
  border-radius: 8px;
  padding: 20px 24px;
  margin-bottom: 20px;
  background: transparent;
  transition: border-color 0.2s ease;
}

.post-card:hover {
  border-color: rgba(128, 128, 128, 0.6);
}

.post-card-title {
  margin: 0 0 10px 0 !important;
  font-size: 1.35rem !important;
  border-bottom: none !important;
}

.post-card-title a {
  text-decoration: none !important;
}

.post-card-title a:hover {
  text-decoration: underline !important;
}

.post-card-excerpt {
  margin: 0 0 14px 0 !important;
  line-height: 1.6 !important;
  opacity: 0.85;
}

.post-card-footer {
  font-size: 0.85rem !important;
  opacity: 0.65;
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  align-items: center;
}

.post-card-footer .sep {
  opacity: 0.4;
}
</style>

{% for post in site.categories.research %}
  {% include card-post.html %}
{% endfor %}
