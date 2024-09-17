<template>
  <section id="projects" class="projects">
    <h2>Projects</h2>
    <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
  </section>
</template>

<script>
import ProjectCard from './ProjectCard.vue'

export default {
  name: 'ProjectsSection',
  components: {
    ProjectCard
  },
  data() {
    return {
      projects: [
        {
          id: 1,
          title: '"전지적 참견시점"',
          description: 'Vue 3와 Spring을 기반으로 개발된 혁신적인 채용정보 사이트',
          period: '2024.08.26 ~ 10.02',
          features: '채용 정보 검색, 이력서 관리, 기업 리뷰 시스템'
        }
        // 추가 프로젝트를 여기에 넣을 수 있습니다.
      ]
    }
  }
}
</script>

<style scoped>
.projects {
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
</style>
