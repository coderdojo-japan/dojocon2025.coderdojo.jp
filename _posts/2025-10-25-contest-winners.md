---
layout: default
date: 2025-10-25
permalink: /contests/winners/
title: DojoCon Japan 2025 プログラミングコンテスト受賞作品一覧
title-in-news-list: プログラミングコンテストの受賞作品が決定しました
tag: コンテスト
categories: news
---

{% include navbar.html %}

<h2 class="mx-auto text-4xl text-center mb-2 mt-30 px-4 sm:px-8 xl:mt-15 break-keep">
  プログラミング<wbr>コンテスト 受賞作品一覧
</h2>

<div class="max-w-2xl mx-auto px-4 sm:px-8 my-15">
  <section class="w-full mx-auto">
    <div class="space-y-15">
      {% for w in site.data.contests_winners.winners %}
        {% assign work = site.data.contests_winners.works[w.work] %}
        <article>
          <div>
            <h3 class="text-3xl mb-4">{{ w.award }}</h3>
            <h4 class="text-2xl mb-2">{{ w.work }}</h4>
          </div>

          <div class="flex justify-center mb-2">
            <img src="{{ work.image }}" alt="{{ w.work }} の画像" class="max-h-90 w-auto max-w-full object-contain rounded-md" />
          </div>
          <p class="text-base mb-1">作: <strong>{{ work.author }}</strong></p>
          <a class="underline text-[#cc8f2e]" href="{{ work.protopedia }}" target="_blank" rel="noopener">ProtoPedia で見る</a>
        </article>
      {% endfor %}
    </div>
  </section>
</div>
