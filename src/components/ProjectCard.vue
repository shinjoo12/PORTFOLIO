<template>
  <div class="project-card">
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
    <p><strong>진행 기간:</strong> {{ project.period }}</p>
    <p><strong>주요 기능:</strong> {{ project.features }}</p>
  </div>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: {
    project: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.project-card {
  background-color: #f9f9f9;
  border-radius: 8px;
  padding: 1.5rem;
  margin-top: 1rem;
  transition: box-shadow 0.3s ease;
}

.project-card:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

h3 {
  color: #3498db;
  margin-bottom: 0.5rem;
}

p {
  margin-bottom: 0.5rem;
}

strong {
  font-weight: bold;
}
</style>
