<script setup>
// 넷플릭스 스타일에는 별도 스크립트 필요 없음
</script>

<template>
  <div class="netflix-app">
    <nav class="navbar">
      <div class="logo">
        <img src="https://upload.wikimedia.org/wikipedia/commons/7/7a/Logonetflix.png" alt="Netflix Logo" />
      </div>
      <ul class="menu">
        <li>홈</li>
        <li>시리즈</li>
        <li>영화</li>
        <li>NEW! 요즘 대세</li>
        <li>내가 찜한 콘텐츠</li>
      </ul>
    </nav>
    <header class="main-banner">
      <div class="banner-content">
        <h1>지금 뜨는 콘텐츠</h1>
        <p>넷플릭스에서 인기 있는 영화와 시리즈를 만나보세요.</p>
        <button>지금 시청하기</button>
      </div>
    </header>
    <section class="content-row">
      <h2>인기 콘텐츠</h2>
      <div class="thumbnails">
        <div class="thumbnail" v-for="n in 10" :key="n">
          <img :src="`https://picsum.photos/200/300?random=${n}`" :alt="`콘텐츠 ${n}`" />
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.netflix-app {
  background: #141414;
  min-height: 100vh;
  color: #fff;
  font-family: 'Noto Sans KR', Arial, Helvetica, sans-serif;
}
.navbar {
  display: flex;
  align-items: center;
  padding: 20px 40px;
  background: rgba(20,20,20,0.95);
}
.logo img {
  height: 38px;
}
.menu {
  display: flex;
  gap: 30px;
  list-style: none;
  margin-left: 40px;
  font-size: 1.1rem;
  padding: 0;
}
.menu li {
  cursor: pointer;
  transition: color 0.2s;
}
.menu li:hover {
  color: #e50914;
}
.main-banner {
  background: url('https://assets.nflxext.com/ffe/siteui/vlv3/6b1e2e2e-2e2e-4e2e-8e2e-2e2e2e2e2e2e/6b1e2e2e-2e2e-4e2e-8e2e-2e2e2e2e2e2e_KR-kr-20240610-popsignuptwoweeks-perspective_alpha_website_large.jpg') center/cover no-repeat;
  height: 420px;
  display: flex;
  align-items: flex-end;
  position: relative;
}
.banner-content {
  background: linear-gradient(180deg, rgba(20,20,20,0.1) 60%, #141414 100%);
  padding: 40px 60px;
}
.banner-content h1 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}
.banner-content p {
  font-size: 1.2rem;
  margin-bottom: 20px;
}
.banner-content button {
  background: #e50914;
  color: #fff;
  border: none;
  padding: 12px 32px;
  font-size: 1.1rem;
  border-radius: 4px;
  cursor: pointer;
  font-weight: bold;
  transition: background 0.2s;
}
.banner-content button:hover {
  background: #b0060f;
}
.content-row {
  margin-top: 40px;
  padding: 0 40px;
}
.content-row h2 {
  font-size: 1.5rem;
  margin-bottom: 18px;
}
.thumbnails {
  display: flex;
  gap: 18px;
  overflow-x: auto;
  padding-bottom: 10px;
}
.thumbnail {
  min-width: 200px;
  border-radius: 6px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0,0,0,0.4);
  transition: transform 0.2s;
}
.thumbnail img {
  width: 100%;
  display: block;
}
.thumbnail:hover {
  transform: scale(1.08);
  z-index: 2;
}
</style>
