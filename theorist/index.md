---
layout: page-banner
title: The Sustainability Theorist
description: Essays on the conceptual foundations of sustainability science—clarifying frameworks, untangling debates, and developing theoretical tools for the field.
banner_image: /assets/images/theorist-banner.svg
wide: true
intro: |-
  Getting theory right matters for sustainability science. The field is a "big tent" made
  out of many different research programs and disciplinary perspectives. Working out the
  theory is how those programs come to share a vocabulary, how they learn from one another
  rather than talking past one another, and, I think, how the field as a whole gets
  stronger.

  The essays here are where I try to work some of that out, with less jargon than a journal
  article allows and (hopefully) more fun to read. Some of the thinking will end up in
  articles eventually; some of it won't. Either way, this is a way to have the discussion
  now. Most are mine, with occasional guests, roughly one a month. Reactions,
  disagreements, and ideas are [very welcome](/harley/).
---

<ul class="post-list">
{% for post in site.posts %}
  <li class="post-card">
    {% if post.image %}
    <a class="post-card-thumb" href="{{ post.url | relative_url }}" aria-hidden="true" tabindex="-1">
      <img src="{{ post.image | relative_url }}" alt="" loading="lazy">
    </a>
    {% endif %}
    <div class="post-card-body">
      <h3 class="post-list-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <p class="post-list-meta">{{ post.date | date: "%B %-d, %Y" }}{% if post.author %} &middot; {{ post.author }}{% endif %}</p>
      {% if post.description %}<p class="post-list-excerpt">{{ post.description }}</p>{% endif %}
    </div>
  </li>
{% endfor %}
</ul>

{% if site.posts.size == 0 %}
<p class="text-muted">No posts yet. Check back soon.</p>
{% endif %}
