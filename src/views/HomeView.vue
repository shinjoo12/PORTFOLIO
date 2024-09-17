<template>
  <div class="home">
    <header class="hero">
      <div class="hero-content">
        <img src="/images/jooyeon.jpg" alt="신주연 프로필 사진" class="profile-image" />
        <div class="hero-text">
          <h1>신주연</h1>
          <h2>백엔드 개발자</h2>
          <p>끊임없는 도전과 혁신으로 서비스의 근간을 다지는 열정적인 백엔드 개발자</p>
        </div>
      </div>
    </header>

    <section class="summary">
      <h2>About Me</h2>
      <p>
        안녕하세요, 끊임없는 도전과 혁신으로 서비스의 근간을 다지는 열정적인 백엔드 개발자
        신주연입니다.
      </p>
      <router-link to="/about" class="btn">더 알아보기</router-link>
    </section>

    <section class="skills-preview">
      <h2>Skills</h2>
      <ul>
        <li>Spring Boot</li>
        <li>Java</li>
        <li>MySQL</li>
        <li>Vue 3</li>
        <li>Flutter</li>
      </ul>
      <router-link to="/skills" class="btn">모든 스킬 보기</router-link>
    </section>

    <section class="projects-preview">
      <h2>Latest Project</h2>
      <div class="project-card">
        <h3>"전지적 참견시점"</h3>
        <p>Vue 3와 Spring을 기반으로 개발된 혁신적인 채용정보 사이트</p>
        <router-link to="/projects" class="btn">프로젝트 더 보기</router-link>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'HomeView'
}
</script>

<style scoped>
.home {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
}

.hero {
  background-color: #f8f9fa;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  margin-bottom: 40px;
  margin-top: 30px;
}

.hero-content {
  display: flex;
  align-items: center;
  padding: 40px;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 40px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: scale(1.05);
}

.hero-text {
  flex: 1;
}

h1 {
  font-size: 2.5em;
  color: #3498db;
  margin-bottom: 10px;
}

h2 {
  font-size: 1.5em;
  color: #333;
  margin-bottom: 15px;
}

section {
  background-color: white;
  border-radius: 10px;
  padding: 30px;
  margin-bottom: 30px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

.btn {
  display: inline-block;
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
  border-radius: 5px;
  transition:
    background-color 0.3s,
    transform 0.3s;
}

.btn:hover {
  background-color: #2980b9;
  transform: translateY(-2px);
}

ul {
  list-style-type: none;
  padding: 0;
  margin-bottom: 20px;
}

li {
  display: inline-block;
  margin-right: 10px;
  margin-bottom: 10px;
  background-color: #e0e0e0;
  padding: 8px 15px;
  border-radius: 20px;
  font-size: 0.9em;
  transition: background-color 0.3s;
}

li:hover {
  background-color: #d0d0d0;
}

.project-card {
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 5px;
  transition: box-shadow 0.3s;
}

.project-card:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

@media (max-width: 768px) {
  .hero-content {
    flex-direction: column;
    text-align: center;
  }

  .profile-image {
    margin-right: 0;
    margin-bottom: 20px;
  }
}
</style>
