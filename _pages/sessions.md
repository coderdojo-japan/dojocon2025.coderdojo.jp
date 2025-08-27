---
layout: default
title: SESSION
subtitle: セッション
permalink: /sessions
---
<h2 id="outline" class="text-4xl text-center mb-8 pt-20">
  セッション
  <span class="block mt-5 text-2xl">SESSIONS</span>
</h2>

<ul class="max-w-7xl px-4 sm:px-8 mx-auto flex flex-wrap justify-between gap-y-16">
  {% for session in site.data.sessions %}
    <li class="w-full sm:w-[46%] sm:min-w-[500px] mx-auto">
      {% if session.news-link %}
        <a href='{{ session.news-link }}'>
          <h3 class="text-2xl mb-2">{{ session.title }}</h3>
        </a>
      {% else %}
        <h3 class="text-2xl mb-2">{{ session.title }}</h3>
      {% endif %}

      {% if session.tag %}
        <span class="block w-fit mb-4 min-w-24 text-center px-4 py-px rounded-xs bg-[#cc8f2e] text-white">{{ session.tag }}</span>
      {% endif %}

      <div class="text-gray-600">
        {{ session.text | markdownify}}
      </div>

      {% if session.news-link %}
        <a class="block w-fit my-2 border rounded p-2" href='{{ session.news-link }}'>
          <i class='fas fa-scroll'></i> 詳細を見る
        </a>
      {% endif %}

      <div class="flex gap-x-4 my-8">
        {% if session.profile-img %}
          <div class="mt-2 w-24 shrink-0">
            {% if session.news-link %}
              <a href='{{ session.news-link }}'>
                <img src="https://placehold.jp/512x512.png" alt="プロフィール画像">
              </a>
            {% else %}
              <img src="https://placehold.jp/512x512.png" alt="プロフィール画像">
            {% endif %}
          </div>
        {% endif %}

        <div class="flex flex-col gap-y-2">
          <p class="text-lg">{{ session.speaker }}</p>

          <p class="text-sm text-gray-800">
            {% if session.affiliation %}
              （{{ session.affiliation }}）
            {% endif %}
          </p>

          {% if session.profile-text %}
            <div class="text-sm text-gray-800 leading-6">
              {{ session.profile-text | markdownify }}
            </div>
          {% endif %}
        </div>
      </div>
    </li>
  {% endfor %}
</ul>
