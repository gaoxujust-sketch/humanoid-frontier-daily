---
title: 首页
nav_order: 0
---

<div class="journal-hero">
  <div class="journal-kicker">HUMANOID &amp; INTELLIGENCE FRONTIER · DAILY</div>
  <h1 class="journal-title">人形与智能前沿日刊</h1>
  <p class="journal-sub">从机器人机械性能工程师的视角，追踪人形机器人全栈的真实进展与通用大模型的智能前沿。不做新闻搬运：每条动态都给出判断、证据边界，以及对团队的启发。</p>
</div>

{% assign issues = site.pages | where_exp: "p", "p.path contains 'issues/'" | sort: "path" | reverse %}
{% assign latest = issues | first %}

## 最新一期

<div class="latest-card">
  <div class="latest-label">LATEST ISSUE</div>
  <a class="latest-title" href="{{ latest.url | relative_url }}">{{ latest.title }}</a>
  <p class="latest-note">头条与「今日一判」见本期正文。手机上速览，电脑上深读。</p>
  <a class="read-btn" href="{{ latest.url | relative_url }}">阅读本期 →</a>
</div>

## 往期目录

<div class="issue-grid">
{% for p in issues %}
  <a class="issue-card" href="{{ p.url | relative_url }}">
    <span class="issue-card-title">{{ p.title }}</span>
    <span class="issue-card-go">阅读全文 →</span>
  </a>
{% endfor %}
</div>

## 栏目

<div class="columns-grid">
  <div class="column-cell"><strong>今日一判</strong><span>当天最重要的一条，直接给结论</span></div>
  <div class="column-cell"><strong>本体</strong><span>新机型、执行器与关节、结构与热、量产进展</span></div>
  <div class="column-cell"><strong>控制</strong><span>全身控制、跌倒恢复、强化学习控制</span></div>
  <div class="column-cell"><strong>具身</strong><span>VLA、世界模型、灵巧操作、数据与 sim-to-real</span></div>
  <div class="column-cell"><strong>大模型</strong><span>通用大模型的能力跃迁，只收重大进展</span></div>
  <div class="column-cell"><strong>值得深读</strong><span>值得花时间的论文与开源项目，<a href="{{ '/deep-reading.html' | relative_url }}">累积清单</a></span></div>
</div>

## 说明

- 本站为日刊的阅读版，与 GitHub 仓库原稿、Muse 日刊主页同步更新，每天早上发布新一期。
- 每条动态均标注实际发布日期与一手来源链接；厂商或作者自报的数字会明确标注，不作已验证事实引用。
- 被误标日期的旧闻、缺乏一手来源的消息不收录，剔除原因记录在当期「本期未收录」一节。
