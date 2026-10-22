---
layout: default
title: Turkish Newsletter
permalink: /newsletter/
---
{% assign turkish_posts = site.posts | where: 'language', 'tr' %}
<main class="home newsletter-page"><section class="home-intro"><p class="eyebrow">UNTRUSTEDINPUT · TURKISH NEWSLETTER</p><h1>AI Security,<br><span>in Turkish.</span></h1><p>A Turkish-language digest of AI Security news, learning notes, research findings and reviews. Technical terms stay in English.</p></section><section class="feed newsletter-feed"><div class="feed-heading"><div><span class="eyebrow">{{ turkish_posts.size }} ISSUES</span><h2>Latest issues</h2></div></div><div class="post-list">{% for post in turkish_posts %}<article class="post-row"><div class="post-date">{{ post.date | date: '%b %-d, %Y' }}</div><div><div class="post-meta"><span>{{ post.category | default: 'Newsletter' }}</span>{% if post.type %}<i>{{ post.type }}</i>{% endif %}</div><h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3><p>{{ post.description | default: post.excerpt | strip_html | truncate: 180 }}</p><a class="read-link" href="{{ post.url | relative_url }}">Read issue ↗</a></div></article>{% endfor %}</div><a class="back-link" href="{{ '/' | relative_url }}">← Back to the English blog</a></section></main>
