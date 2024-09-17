<template>
  <section id="about" class="about">
    <div class="about-content">
      <div class="text-content">
        <h2>About Me</h2>
        <p>끊임없는 도전과 혁신으로 서비스의 근간을 다지는 열정적인 백엔드 개발자 신주연입니다.</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection'
}
</script>

<style scoped>
.about {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  padding: 3rem;
  margin: 4rem auto;
  max-width: 900px;
}

.about-content {
  display: flex;
  align-items: center;
  gap: 3rem;
}

.profile-image {
  flex: 0 0 250px;
  position: relative;
  overflow: hidden;
  border-radius: 8px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.profile-image img {
  width: 100%;
  height: auto;
  display: block;
  transition: transform 0.3s ease;
}

.profile-image:hover img {
  transform: scale(1.05);
}

.text-content {
  flex: 1;
}

h2 {
  color: #3498db;
  margin-bottom: 1.5rem;
  font-size: 2.2rem;
}

p {
  line-height: 1.8;
  font-size: 1.1rem;
  color: #34495e;
}

@media (max-width: 768px) {
  .about-content {
    flex-direction: column;
    text-align: center;
  }

  .profile-image {
    margin-bottom: 2rem;
  }
}
</style>
