---
layout: page
title: Seminars
permalink: /seminars/
---

## Seminar Archive

<ul>
  {% for seminar in site.seminars %}
    <li>
      <a href="{{ seminar.url | relative_url }}">{{ seminar.title }}</a>
      — {{ seminar.date | date: "%B %d, %Y" }}
    </li>
  {% endfor %}
</ul>

