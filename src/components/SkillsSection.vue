<template>
  <section id="skills" class="skills">
    <h2>Skills</h2>
    <ul>
      <li v-for="skill in skills" :key="skill">{{ skill }}</li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'SkillsSection',
  data() {
    return {
      skills: ['Spring Boot', 'MySQL', 'Java', 'HTML/CSS', 'Vue 3', 'Flutter']
    }
  }
}
</script>

<style scoped>
.skills {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 2rem;
  margin-bottom: 2rem;
  max-width: 800px;
  margin: 2rem auto;
}

h2 {
  color: #3498db;
  margin-bottom: 1rem;
}

ul {
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  gap: 1rem;
}

li {
  background-color: #3498db;
  color: #fff;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.9rem;
}
</style>
