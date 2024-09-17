<template>
  <div class="about">
    <div class="profile-container">
      <img src="/images/jooyeon.jpg" alt="신주연 프로필 사진" class="profile-image" />
    </div>
    <div class="content">
      <h1>About Me</h1>
      <p>
        안녕하세요, 끊임없는 도전과 혁신으로 서비스의 근간을 다지는 열정적인 백엔드 개발자
        신주연입니다. 저는 현재 하이미디어 국비지원학원에서 백엔드 개발 과정을 수강하며, 기술의
        깊이를 더해가고 있습니다. <br />
      </p>
      <P>
        저에게 있어 백엔드 개발은 사용자 경험의 근간을 설계하고, 비즈니스 로직을 효율적으로
        구현하며, 데이터의 흐름을 최적화하는 기술이기에 이러한 관점에서 저는 항상 더 나은 해결책을
        찾기 위해 끊임없이 고민합니다. 특히, 저는 다음과 같은 영역에 큰 관심을 가지고 있습니다:
      </P>
      <p>
        1. 확장 가능한 아키텍처 설계: 미래의 성장을 고려한 유연하고 확장 가능한 시스템 구축<br />
        2.데이터베이스 최적화: 효율적인 쿼리 작성과 인덱싱을 통한 데이터베이스 성능 향상 <br />3.
        API 개발 및 통합: RESTful API 설계 및 구현, 마이크로서비스 아키텍처 탐구 <br />4. 보안 및
        인증: 안전한 사용자 인증 시스템 구축 및 데이터 보안 강화
      </p>
      <p>
        제 목표는 단순히 기능을 구현하는 개발자를 넘어, 서비스의 가치를 극대화하고 사용자에게 의미
        있는 경험을 제공하는 백엔드 전문가로 성장하는 것입니다. 이를 위해 지속적인 학습과 실전
        프로젝트 경험을 통해 기술적 역량을 높이고, 동료들과의 협업을 통해 커뮤니케이션 능력도 함께
        발전시켜 나가고 있습니다. 앞으로도 끊임없는 도전과 성장을 통해 더 나은 서비스, 더 나은
        사용자 경험을 만들어 나가겠습니다.
      </p>
      <p>
        백엔드 개발에 주력하고 있지만, 풀스택 개발자로 성장하기 위해 프론트엔드 기술도 학습하고
        있습니다.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutView'
}
</script>

<style scoped>
.about {
  max-width: 800px;
  margin: 70px auto 0;
  padding: 20px;
  display: flex;
  align-items: flex-start;
  gap: 30px;
}

.profile-container {
  flex-shrink: 0;
}

.profile-image {
  width: 200px;
  height: 200px;
  object-fit: cover;
  border-radius: 50%;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  margin-top: 35px;
}

.profile-image:hover {
  transform: scale(1.05);
}

.content {
  flex-grow: 1;
}

h1 {
  color: #3498db;
  margin-bottom: 20px;
}

p {
  margin-bottom: 15px;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .about {
    flex-direction: column;
    align-items: center;
  }

  .profile-container {
    margin-bottom: 20px;
  }
}
</style>
