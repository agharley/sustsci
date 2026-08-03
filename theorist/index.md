---
layout: page-banner
title: The Sustainability Theorist
description: Essays on the conceptual foundations of sustainability science—clarifying frameworks, untangling debates, and developing theoretical tools for the field.
banner_image: /assets/images/theorist-banner.svg
wide: true
intro: >-
  Getting theory right matters for sustainability science: it is how a field built from
  many research programs manages to work together, and how we stay clear about what we are
  all working toward. The essays here take up the kinds of questions that sit underneath a
  lot of work in the field. How should we think about the difference between inequality and
  inequity? Why do unsustainable development pathways persist even when we have the data and
  the public will to transform toward more sustainable ones? How have people across
  centuries, cultures, and religious traditions understood what one generation owes the
  next? Some of the thinking will end up in journal articles eventually; some of it won't.
  Either way, the essays are a way to have the discussion now, with less academic jargon and
  convention, accessible (and hopefully more fun to read) for a wider audience. Most are
  mine, with occasional guest essays, roughly one a month. Reactions, disagreements, and
  ideas are [very welcome](/harley/).
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
