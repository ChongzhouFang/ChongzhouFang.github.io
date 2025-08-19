---
layout: archive
title: "Students"
permalink: /students/
author_profile: false
---

<div class="students-grid">
  {% for student in site.students %}
    <div class="student-card">
      {% if student.photo %}
        <img class="student-photo" src="{{ student.photo }}" alt="{{ student.name }}" />
      {% endif %}
      <h3>{{ student.name }}</h3>
      <p><strong>Starting:</strong> {{ student.starting }}</p>
      <p><strong>Research Area:</strong> {{ student.area }}</p>
    </div>
  {% endfor %}
</div>

<style>
.student-photo {
  width: 250px;   /* shrink image */
  height: auto;   /* keep proportions */
  border-radius: 8px;
}
.students-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1.5rem;
}
.student-card {
  max-width: 200px;
  text-align: center;
}
</style>