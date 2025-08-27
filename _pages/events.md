---
layout: default
permalink: /events/
---
<h2 id="outline" class="text-4xl text-center mb-8 pt-40 xl:pt-20">
  企画
  <span class="block mt-5 text-2xl">EVENTS</span>
</h2>

<ul class="max-w-7xl px-4 sm:px-8 mx-auto flex flex-wrap justify-between gap-y-16">
  {% for event in site.data.events %}
    <li class="w-full sm:w-[46%] sm:min-w-[500px] mx-auto">
      {% if event.news-link %}
        <a href='{{ event.news-link }}'>
          <h3 class="text-2xl mb-2">{{ event.title }}</h3>
        </a>
      {% else %}
        <h3 class="text-2xl mb-2">{{ event.title }}</h3>
      {% endif %}

      {% if event.tag %}
        <span class="block w-fit mb-4 min-w-24 text-center px-4 py-px rounded-xs bg-[#cc8f2e] text-white">{{ event.tag }}</span>
      {% endif %}

      <div class="text-gray-600">
        {{ event.text | markdownify}}
      </div>

      {% if event.url %}
        <a class="block w-fit my-2 border rounded p-2" href='{{ event.url }}'>
          <i class='fas fa-scroll'></i> 詳細を見る
        </a>
      {% endif %}

      <div class="flex gap-x-4 my-8">
        <img src="{{ event.img }}" />
      </div>
    </li>
  {% endfor %}
</ul>
