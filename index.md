---
layout: default
---

<div class="home">

  <h1 class="page-heading">Posts</h1>

  <ul id="postcontext" class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title | escape }}</a>
        </h2>

        <ul id="tagcontext" class="tags">
        {% for tag in post.tags %}
          <li><a href="/tags#{{ tag }}" class="tag">{{ tag }}</a></li>
        {% endfor %}
        </ul>

      </li>
    {% endfor %}
  </ul>

</div>
