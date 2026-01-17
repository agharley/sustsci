---
layout: page-banner
title: The Sustainability Theorist
subtitle: Essays on sustainability science theory and practice
description: Essays on the conceptual foundations of sustainability science—clarifying frameworks, untangling debates, and developing theoretical tools for the field.
banner_image: /assets/images/theorist-banner.svg
---

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <h3 class="post-list-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <p class="post-list-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
  </li>
{% endfor %}
</ul>

{% if site.posts.size == 0 %}
<p class="text-muted">No posts yet. Check back soon.</p>
{% endif %}
