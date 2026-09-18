---
permalink: /blog/
title: ""
author_profile: false
---

<script src="https://cdn.tailwindcss.com"></script>
<script src="https://unpkg.com/lucide@latest"></script>

<div class="w-full max-w-2xl mx-auto px-4 sm:px-6 py-4 text-slate-200 font-sans antialiased">

  <div class="mb-8">
    <h1 class="text-2xl font-bold text-slate-100 tracking-tight mb-2">Blog</h1>
    <p class="text-sm text-slate-400 leading-relaxed">
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
      <div class="bg-[#111827]/60 border border-slate-800 rounded-xl p-8 text-center">
        <div class="w-10 h-10 rounded-lg bg-slate-800/50 border border-slate-700/40 flex items-center justify-center text-slate-400 mx-auto mb-3">
          <i data-lucide="pen-tool" class="w-5 h-5"></i>
        </div>
        <h3 class="text-sm font-semibold text-slate-200 mb-1">No Articles Published Yet</h3>
        <p class="text-xs text-slate-400 max-w-sm mx-auto leading-relaxed">
          Technical analyses and field notes will appear here once new posts are committed to the repository.
        </p>
      </div>
    {% endif %}
  </div>

</div>

<script>
  lucide.createIcons();
</script>
