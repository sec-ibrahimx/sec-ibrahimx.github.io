---
layout: clean
permalink: /blog/
---

<div class="mb-10">
  <h1 class="text-2xl font-bold text-slate-100 tracking-tight mb-2">Blog</h1>
  <p class="text-sm text-slate-400 leading-relaxed max-w-xl">
    Technical write-ups, engineering notes, and analytical observations across systems, networking, and applied AI security.
  </p>
</div>

<div class="space-y-4">
  {% assign blog_posts = site.posts | where_exp: "item", "item.categories contains 'blog'" %}
  {% if blog_posts.size > 0 %}
    {% for post in blog_posts %}
      {% include card-post.html %}
    {% endfor %}
  {% else %}
    <div class="rounded-xl border border-slate-800/60 bg-[#111827]/40 p-6 text-center">
      <p class="text-sm text-slate-500">No articles published yet. New write-ups will appear here soon.</p>
    </div>
  {% endif %}
</div>
