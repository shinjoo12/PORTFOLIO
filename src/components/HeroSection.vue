<template>
  <section class="hero">
    <div class="hero-content">
      <div class="text-content">
        <div class="profile-image">
          <img src="/images/jooyeon.jpg" alt="신주연 프로필 사진" />
        </div>
        <h1>신주연</h1>
        <h2>백엔드 신입 개발자</h2>
        <p>끊임없는 도전과 혁신으로 서비스의 근간을 다지는 열정적인 백엔드 개발자</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection'
}
</script>

<style scoped>
.hero {
  background-color: #f8f9fa;
  color: #333;
  padding: 6rem 0;
}

.hero-content {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.profile-image {
  flex: 0 0 300px;
  margin-right: 4rem;
  position: relative;
  overflow: hidden;
  border-radius: 15px;
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
}

.profile-image::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(45deg, rgba(52, 152, 219, 0.3), rgba(41, 128, 185, 0.3));
  z-index: 1;
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

h1 {
  font-size: 3.5rem;
  margin-bottom: 0.5rem;
  color: #3498db;
}

h2 {
  font-size: 1.8rem;
  font-weight: 300;
  margin-bottom: 1rem;
  color: #2c3e50;
}

p {
  font-size: 1.2rem;
  max-width: 600px;
  line-height: 1.6;
  color: #34495e;
}

@media (max-width: 768px) {
  .hero-content {
    flex-direction: column;
    text-align: center;
  }

  .profile-image {
    margin-right: 0;
    margin-bottom: 2rem;
    max-width: 250px;
  }

  .text-content {
    text-align: center;
  }
}
</style>
