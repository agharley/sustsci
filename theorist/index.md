---
layout: page-banner
title: The Sustainability Theorist
subtitle: Essays on sustainability science theory and practice
description: Essays on the conceptual foundations of sustainability science—clarifying frameworks, untangling debates, and developing theoretical tools for the field.
banner_image: /assets/images/theorist-banner.svg
wide: true
---

Getting theory right matters for sustainability science. The essays here work through questions the field needs clearer thinking on: how should we think about the difference between inequality and inequity? How have people across centuries, cultures, and religious traditions understood what one generation owes the next? Some of this thinking is on its way to becoming journal articles; some of it will only ever live here. Either way, this is a place to have the discussion now, with less of the jargon and convention of academic prose: more accessible, and I hope more fun to read, for a wider audience. Roughly one essay a month; most are mine, with occasional guest essays. Reactions, disagreements, and ideas are [very welcome]({{ '/harley/' | relative_url }}).

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
