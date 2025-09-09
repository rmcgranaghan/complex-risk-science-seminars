---
layout: seminar
title: Seminars
permalink: /seminars/
---

## Upcoming Seminars

<ul>
  {% assign upcoming = site.seminars | where_exp: "s", "s.date >= site.time" | sort: "date" %}
  {% for seminar in upcoming %}
    <li>
      <a href="{{ seminar.url | relative_url }}">{{ seminar.title }}</a><br/>
      {{ seminar.speaker }} — {{ seminar.date | date: "%B %d, %Y" }} at {{ seminar.time }}
    </li>
  {% endfor %}
</ul>

## Past Seminars

<ul>
  {% assign past = site.seminars | where_exp: "s", "s.date < site.time" | sort: "date" | reverse %}
  {% for seminar in past %}
    <li>
      <a href="{{ seminar.url | relative_url }}">{{ seminar.title }}</a><br/>
      {{ seminar.speaker }} — {{ seminar.date | date: "%B %d, %Y" }}
    </li>
  {% endfor %}
</ul>


