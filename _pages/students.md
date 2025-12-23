---
layout: archive
title: "Students"
permalink: /students/
author_profile: false
---

<style>
.students-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 24px;
}

.student-card {
  text-align: center;
}

.student-card img {
  width: 150px;
  border-radius: 8px;
}
</style>

{% include base_path %}
<div class="students-grid">
  {% for student in site.students %}
    <div class="student-card">
      {% if student.photo %}
        <img src="{{ student.photo | relative_url }}"
             alt="{{ student.name }}" />
      {% endif %}
      <h3>{{ student.name }}</h3>
      <p><strong>Starting:</strong> {{ student.starting }}</p>
      <p><strong>Research Area:</strong> {{ student.area }}</p>
    </div>
  {% endfor %}
</div>
