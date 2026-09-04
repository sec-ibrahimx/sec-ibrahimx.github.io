---
layout: default
permalink: /projects/
title: ""
author_profile: false
---

<script src="https://cdn.tailwindcss.com"></script>
<script src="https://unpkg.com/lucide@latest"></script>

<div class="w-full max-w-2xl mx-auto px-4 sm:px-6 py-4 text-slate-200 font-sans antialiased">

  <div class="mb-8">
    <h1 class="text-xl font-bold text-slate-100 tracking-normal mb-2">Projects</h1>
    <p class="text-sm text-slate-400 leading-relaxed">
      Applied security tooling, experimental systems implementations, and empirical proof-of-concepts.
    </p>
  </div>

  <div class="space-y-4">
    {% for post in site.categories.projects %}
      {% include card-post.html %}
    {% endfor %}
  </div>

</div>

<script>
  lucide.createIcons();
</script>
