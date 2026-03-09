---
layout: homepage
---

## Blog

<div class="blog-list">
{% assign sorted_posts = site.posts | sort: 'date' | reverse %}
{% for post in sorted_posts %}
<div class="blog-entry">
  <p>
    <strong><a href="{{ post.url | relative_url }}">{{ post.title }}</a></strong><br>
    <small>{{ post.date | date: "%B %-d, %Y" }}</small><br>
    {% if post.subtitle %}<em>{{ post.subtitle }}</em>{% endif %}
  </p>
</div>
{% endfor %}
</div>
