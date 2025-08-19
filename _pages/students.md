---
layout: archive
title: "Students"
permalink: /students/
author_profile: false
---

{% include base_path %}
<div>
  {% for student in site.students %}
    <div>
      {% if student.photo %}
        <img src="{{ student.photo }}" alt="{{ student.name }}" style="width:150px; height:auto; border-radius:8px;" />
      {% endif %}
      <h3>{{ student.name }}</h3>
      <p><strong>Starting:</strong> {{ student.starting }}</p>
      <p><strong>Research Area:</strong> {{ student.area }}</p>
    </div>
  {% endfor %}
</div>