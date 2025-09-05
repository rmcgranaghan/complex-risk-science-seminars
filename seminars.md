---
layout: default
title: Public Seminar Series
---

# Public Seminar Series

Join us for engaging talks at the intersection of science, technology, and society.

---

## Upcoming Seminars

{% assign upcoming = site.seminars | where_exp: "s", "s.date >= site.time" | sort: "date" %}
{% for seminar in upcoming %}
### [{{ seminar.title }}]({{ seminar.url }})
*Speaker:* {{ seminar.speaker }} ({{ seminar.institution }})  
*Date:* {{ seminar.date | date: "%B %d, %Y — %I:%M %p %Z" }}

{{ seminar.description }}

---
{% endfor %}

## Past Seminars

{% assign past = site.seminars | where_exp: "s", "s.date < site.time" | sort: "date" | reverse %}
{% for seminar in past %}
- **[{{ seminar.title }}]({{ seminar.url }})** — {{ seminar.speaker }} ({{ seminar.date | date: "%B %d, %Y" }})
  {% if seminar.recording %}[Watch Recording]({{ seminar.recording }}){% endif %}
{% endfor %}
