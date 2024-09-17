<template>
  <div class="skills">
    <h1>My Skills</h1>
    <div v-for="(category, categoryName) in skills" :key="categoryName" class="skill-category">
      <h2>{{ categoryName }}</h2>
      <div v-for="skill in category" :key="skill.name" class="skill-item">
        <span class="skill-name">{{ skill.name }}</span>
        <div class="skill-bar">
          <div class="skill-level" :style="{ width: `${skill.level}%` }"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SkillsView',
  data() {
    return {
      skills: {
        Backend: [
          { name: 'Spring Boot', level: 85 },
          { name: 'Java', level: 85 },
          { name: 'MySQL', level: 75 },
          { name: 'Spring Security', level: 70 },
          { name: 'RESTful API', level: 75 }
        ],
        Frontend: [
          { name: 'HTML/CSS', level: 70 },
          { name: 'Vue 3', level: 85 },
          { name: 'JavaScript', level: 60 }
        ],
        Mobile: [{ name: 'Flutter', level: 50 }],
        'Tools & DevOps': [
          { name: 'Git', level: 70 },
          { name: 'GitHub', level: 75 },
          { name: 'IntelliJ IDEA', level: 80 },
          { name: 'Visual Studio Code', level: 75 },
          { name: 'Docker', level: 60 },
          { name: 'Jenkins', level: 55 },
          { name: 'Vercel', level: 65 },
          { name: 'JSON Web Token', level: 70 }
        ]
      }
    }
  }
}
</script>

<style scoped>
.skills {
  max-width: 800px;
  margin: 30px auto;
  padding: 20px;
}

h1 {
  color: #3498db;
  margin-bottom: 20px;
}

.skill-category {
  margin-bottom: 30px;
}

h2 {
  color: #3498db;
  margin-bottom: 15px;
}

.skill-item {
  margin-bottom: 10px;
}

.skill-name {
  display: inline-block;
  width: 150px;
  font-weight: bold;
}

.skill-bar {
  display: inline-block;
  width: calc(100% - 160px);
  height: 20px;
  background-color: #e0e0e0;
  border-radius: 10px;
  overflow: hidden;
}

.skill-level {
  height: 100%;
  background-color: #3498db;
  border-radius: 10px;
}
</style>
