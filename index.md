---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}

{% for post in site.posts limit:1 %}
  <div id="post">
    <h1>{{ post.title }}</h1>
    <p class="meta">
      {{ post.date | date_to_string }}
      {% if post.location %}{{ post.location }}{% endif %}
    </p>
    {{ post.content }}
  </div>
{% endfor %}

## Recent posts
<ul class="posts">
  {% for post in site.posts limit:10 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
