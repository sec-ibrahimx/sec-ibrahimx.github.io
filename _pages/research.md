---
layout: nabla-page
permalink: /research/
title: "Research & Papers"
subtitle: "Breakdowns, gap analyses, and critical reviews of security and AI literature."
icon: doc
author_profile: false
---

<script src="https://cdn.tailwindcss.com"></script>
<script src="https://unpkg.com/lucide@latest"></script>

<div class="w-full max-w-2xl mx-auto px-4 sm:px-6 py-4 text-slate-200 font-sans antialiased">


  <div class="space-y-4">
    {% for post in site.categories.research %}
      {% include card-post.html %}
    {% endfor %}
  </div>

</div>

<script>
  lucide.createIcons();
</script>
