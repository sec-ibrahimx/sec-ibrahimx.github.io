---
layout: default
permalink: /blog/
title: ""
author_profile: false
sidebar: false
classes: wide
---

<style>
  /* إخفاء البروفايل الجانبي وتوسيط الصفحة قسرياً */
  .sidebar, .author__avatar, .sidebar__right {
    display: none !important;
  }
  #main {
    margin-left: auto !important;
    margin-right: auto !important;
    padding-left: 0 !important;
    padding-right: 0 !important;
    max-width: 100% !important;
    width: 100% !important;
  }
  .page__inner-wrap {
    float: none !important;
    margin: 0 auto !important;
    width: 100% !important;
  }
</style>

<script src="https://cdn.tailwindcss.com"></script>
<script src="https://unpkg.com/lucide@latest"></script>

<div class="w-full max-w-2xl mx-auto px-4 sm:px-6 py-4 text-slate-200 font-sans antialiased">

  <div class="mb-8">
    <h1 class="text-xl font-bold text-slate-100 tracking-normal mb-2">Blog</h1>
    <p class="text-sm text-slate-400 leading-relaxed">
      Technical thoughts, reflections, and write-ups on cybersecurity, systems, and research.
    </p>
  </div>

  <div class="space-y-4">
    {% for post in site.posts %}
      {% include card-post.html %}
    {% endfor %}
  </div>

</div>

<script>
  lucide.createIcons();
</script>
