---
layout: page
title: Team
---

# Meet the Team

{% assign team = 
  [
    {
      "name": "Sarolt Kinga Gintner",
      "image": "/assets/images/Kinga.JPEG",
      "bio": "I hold an MSc in Biology from Eötvös Loránd University (ELTE TTK). In the HillierLab research group, I am responsible for animal care and welfare, while my research focuses on the vision-based aspects of animal behavior."
    },
    {
      "name": "Barna Kovacs",
      "image": "/assets/images/Barna.jpg",
      "bio": "I mainly work on the development side, so my strengths are in programming areas like data analysis and computational modelling. I enjoy spending my free time in nature, especially when it snows a little, and by playing board games."
    },
    {
      "name": "Fanni Soos",
      "image": "/assets/images/Fanni.jpg",
      "bio": "As a laboratory assistant in our group, I take part in processing and analyzing experimental samples in the anatomy lab."
    }
  ]
%}

<div class="team-container">
  {% for member in team %}
    <div class="team-member {% if forloop.index0 modulo 2 == 0 %}left{% else %}right{% endif %}">
      <img src="{{ member.image }}" alt="{{ member.name }}">
      <div class="bio">
        <h2>{{ member.name }}</h2>
        <p>{{ member.bio }}</p>
      </div>
    </div>
  {% endfor %}
</div>

<style>
.team-container {
  display: flex;
  flex-direction: column;
  gap: 3rem;
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 1rem;
}

.team-member {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.team-member img {
  width: 180px;
  height: 180px;
  object-fit: cover;
  border-radius: 50%;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.team-member.left {
  flex-direction: row;
}

.team-member.right {
  flex-direction: row-reverse;
}

.team-member .bio {
  max-width: 600px;
}

.team-member h2 {
  margin-top: 0;
  margin-bottom: 0.5rem;
}

@media (max-width: 700px) {
  .team-member {
    flex-direction: column !important;
    text-align: center;
  }
}
</style>
