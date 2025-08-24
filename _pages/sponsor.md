---
layout: default
permalink: /news
---
<h2 class="text-4xl text-center mb-8 pt-20">
  お知らせ
  <span class="block mt-5 text-2xl">NEWS</span>
</h2>

<div class="max-w-248 mx-auto px-8 flex flex-wrap *:w-[48%] gap-y-8 justify-between">
  {% for post in site.posts %}
    {% include articles.html %}
  {% endfor %}
</div>
