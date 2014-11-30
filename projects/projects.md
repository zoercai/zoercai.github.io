---
layout: default
title: Projects
permalink: /projects/
published: true
---

<div class="home">

  <h1 class="page-heading">Projects</h1>

  <ul class="post-list">
    {% for project in site.projects %}
      <li>
        <span class="post-meta">{{ project.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ project.url | prepend: site.baseurl }}">{{ project.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
