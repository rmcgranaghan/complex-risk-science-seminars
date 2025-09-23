---
layout: default
title: Resources
permalink: /resources/
---

# Resources curated from or related to the semninar series
- [JPL's Science Understanding from Data Science (SUDS) Initiative](https://www.jpl.nasa.gov/go/suds/)
- [Awesome Multi-Hazards library](https://github.com/rmcgranaghan/awesome-multihazard/): A curated list of multi-hazard science, analysis, application, and impact
- [Knowledge Action Network on Emergent Risks and Extreme Events](https://www.risk-kan.org/): A group addressing systemic emergent and cascading risks under global and societal change while building knowledge on disaster risk reduction and providing an open platform to scientists across disciplines.
- [MultiSector Dynamics](https://multisectordynamics.org/): A multi-disciplinary collective of researchers based at universities and national labs across the United States to establish a community of practice of MultiSector Dynamics (MSD) researchers and improve our understanding of the co-evolution of human and natural systems over time, and build the next generation of tools that bridge across sectors (energy, water, land, economy) and scales (spatial, temporal), and offer a holistic view of systems-of-systems.
- [Report](https://zenodo.org/records/17122711) from the June 9, 2025 “Complex Risk Science Summit” in Boston that details the key dialectics for Complex Risk Science and Analysis Working Groups that can begin responding to them] (and [here](https://ai.northeastern.edu/event/boston-area-complex-risk-science-exploring-new-frontiers-and-a-new-community-for-understanding-risk) is the link to the Boston Risk Science Summit page).
- _more coming_


---

# Resources by Seminar


{% assign past_seminars = site.seminars | where_exp: "s", "s.date < site.time" | sort: "date" | reverse %}
{% for seminar in past_seminars %}
  {% if seminar.resources %}
  ## [{{ seminar.title }}]({{ seminar.url | relative_url }})
  *{{ seminar.speaker }} — {{ seminar.date | date: "%B %d, %Y" }}*

  <ul>
    {% for r in seminar.resources %}
      <li>
        <a href="{{ r.url }}" target="_blank">{{ r.name }}</a><br>
        <small>{{ r.description }}</small>
      </li>
    {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

