<script setup>
// 특별한 로직 없음
</script>

<template>
  <div class="netflix-app">
    <header class="netflix-header">
      <img class="netflix-logo" src="https://assets.nflxext.com/us/ffe/siteui/common/pngs/nflxlogo.png" alt="Netflix Logo" />
      <nav class="netflix-nav">
        <a href="#">홈</a>
        <a href="#">시리즈</a>
        <a href="#">영화</a>
        <a href="#">NEW! 요즘 대세 콘텐츠</a>
        <a href="#">내가 찜한 리스트</a>
      </nav>
    </header>
    <main class="netflix-main">
      <section class="hero">
        <img class="hero-bg" src="https://assets.nflxext.com/ffe/siteui/vlv3/7e7e7e/2023-11-07-kr-landing-bg.jpg" alt="Netflix Hero" />
        <div class="hero-content">
          <h1>지금 뜨는 콘텐츠</h1>
          <p>넷플릭스에서 인기 있는 영화와 시리즈를 만나보세요.</p>
        </div>
      </section>
      <section class="popular">
        <h2>인기 콘텐츠</h2>
        <div class="popular-list">
          <div class="popular-item" v-for="n in 6" :key="n">
            <img :src="`https://picsum.photos/200/300?random=${n}`" :alt="`콘텐츠 ${n}`" />
            <p>콘텐츠 {{ n }}</p>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<style scoped>
.netflix-app {
  background: #141414;
  color: #fff;
  min-height: 100vh;
  font-family: 'Noto Sans KR', Arial, sans-serif;
}
.netflix-header {
  display: flex;
  align-items: center;
  padding: 20px 40px;
  background: rgba(20, 20, 20, 0.9);
}
.netflix-logo {
  height: 40px;
  margin-right: 40px;
}
.netflix-nav a {
  color: #fff;
  margin-right: 24px;
  text-decoration: none;
  font-weight: 500;
  font-size: 1.1rem;
}
.netflix-nav a:hover {
  text-decoration: underline;
}
.hero {
  position: relative;
  height: 400px;
  display: flex;
  align-items: flex-end;
  justify-content: flex-start;
}
.hero-bg {
  position: absolute;
  top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; z-index: 1;
  filter: brightness(0.5);
}
.hero-content {
  position: relative;
  z-index: 2;
  padding: 40px;
}
.hero-content h1 {
  font-size: 2.5rem;
  margin-bottom: 12px;
}
.popular {
  padding: 40px;
}
.popular-list {
  display: flex;
  gap: 24px;
  margin-top: 20px;
}
.popular-item {
  background: #222;
  border-radius: 8px;
  overflow: hidden;
  width: 200px;
  text-align: center;
  box-shadow: 0 2px 8px rgba(0,0,0,0.3);
}
.popular-item img {
  width: 100%;
  height: 300px;
  object-fit: cover;
}
.popular-item p {
  margin: 12px 0;
  font-size: 1rem;
}
</style>
