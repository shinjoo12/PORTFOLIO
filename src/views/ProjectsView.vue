<template>
  <div class="projects">
    <h1>My Projects</h1>
    <div v-for="project in projects" :key="project.id" class="project-card">
      <h2>{{ project.title }}</h2>
      <p><strong>기간:</strong> {{ project.period }}</p>
      <p>{{ project.description }}</p>
      <p class="github-link">
        <strong>GitHub:</strong>
        <a :href="project.githubLink" target="_blank" rel="noopener noreferrer">{{
          project.githubLink
        }}</a>
      </p>
      <h3>프로젝트 목적:</h3>
      <ul>
        <li v-for="purpose in project.purposes" :key="purpose">{{ purpose }}</li>
      </ul>
      <h3>주요 기능:</h3>
      <ul>
        <li v-for="feature in project.features" :key="feature">{{ feature }}</li>
      </ul>
      <h3>내가 구현한 기능:</h3>
      <ul>
        <li v-for="myFeature in project.myFeatures" :key="myFeature">{{ myFeature }}</li>
      </ul>
      <p><strong>사용 기술:</strong> {{ project.technologies.join(', ') }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectsView',
  data() {
    return {
      projects: [
        {
          id: 1,
          title: '전지적 구직자 시점(전직자)',
          period: '2024.08.26 ~ 10.02',
          description:
            'Vue3와 Spring을 기반으로 개발된 혁신적인 채용정보 사이트입니다. 공공데이터포털의 자격증 API와 채용 API를 활용하여, 최신 채용 정보를 신속하고 효율적으로 제공합니다. 특히, 자격증과 관련된 채용정보를 즉시 확인할 수 있는 기능을 중점적으로 제공하여, 구직자들이 보다 쉽게 자신에게 적합한 채용 기회를 찾을 수 있도록 돕습니다.',
          githubLink: 'https://github.com/Omniscient-Job-Project',
          purposes: [
            '정확하고 신뢰할 수 있는 정보 제공',
            '자격증 기반 채용 정보 강화',
            '사용자 맞춤형 정보 제공',
            '편리한 접근성과 사용자 경험'
          ],
          features: ['자격증 연계 채용 정보 검색', '맞춤형 채용 정보 필터링', '이력서 관리'],
          myFeatures: ['공지사항 기능 구현', '회원가입 기능 구현', '로그인 기능 구현'],
          technologies: ['Vue 3', 'Spring Boot', 'MySQL', 'REST API', 'HTML/CSS', 'JAVASCRIPT']
        }
      ]
    }
  }
}
</script>

<style scoped>
.projects {
  max-width: 800px;
  margin: 30px auto;
  padding: 20px;
}

h1 {
  color: #3498db;
  margin-bottom: 20px;
}

.project-card {
  background-color: #f8f8f8;
  border-radius: 8px;
  padding: 20px;
  margin-bottom: 20px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

h2 {
  color: #3498db;
  margin-bottom: 10px;
}

h3 {
  color: #2c3e50;
  margin-top: 15px;
  margin-bottom: 10px;
}

ul {
  padding-left: 20px;
  margin-bottom: 15px;
}

li {
  margin-bottom: 5px;
}

p {
  margin-bottom: 10px;
  line-height: 1.6;
}

strong {
  color: #2c3e50;
}

.github-link {
  margin-top: 10px;
  font-weight: bold;
}

.github-link a {
  color: #3498db;
  text-decoration: none;
  transition: color 0.3s ease;
}

.github-link a:hover {
  color: #2980b9;
  text-decoration: underline;
}
</style>
