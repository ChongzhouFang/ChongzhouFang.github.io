---
layout: archive
title: "Students"
permalink: /students/
author_profile: true
---

{% include base_path %}

<div class="students-grid">
  {% for student in site.students %}
    <div class="student-card">
      {% if student.photo %}
        <img src="{{ student.photo | relative_url }}" alt="{{ student.name }}" class="student-photo"/>
      {% endif %}
      <h3>{{ student.name }}</h3>
      <p><strong>Starting:</strong> {{ student.starting }}</p>
      <p><strong>Research Area:</strong> {{ student.area }}</p>
    </div>
  {% endfor %}
</div>