---
layout: clean
permalink: /blog/
---

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
