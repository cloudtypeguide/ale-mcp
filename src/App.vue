<script setup>
// 특별한 로직 없음
</script>

<template>
  <div class="netflix-root">
    <header class="netflix-header">
      <img class="logo" src="/src/assets/netflix-logo.png" alt="Netflix" />
      <nav class="nav">
        <a href="#">홈</a>
        <a href="#">시리즈</a>
        <a href="#">영화</a>
        <a href="#">NEW! 요즘 대세 콘텐츠</a>
        <a href="#">내가 찜한 리스트</a>
      </nav>
      <div class="profile">
        <img class="avatar" src="https://randomuser.me/api/portraits/men/32.jpg" alt="Profile" />
      </div>
    </header>
    <main class="main-banner">
      <div class="banner-content">
        <h1>지금 뜨는 콘텐츠</h1>
        <p>넷플릭스에서 인기 있는 시리즈와 영화를 만나보세요.</p>
        <div class="banner-buttons">
          <button>재생</button>
          <button>내가 찜한 리스트</button>
        </div>
      </div>
    </main>
    <section class="content-section">
      <h2>인기 콘텐츠</h2>
      <div class="content-row">
        <img v-for="n in 8" :key="n" :src="`https://image.tmdb.org/t/p/w500/${n}a.jpg`" class="content-thumb" alt="콘텐츠 썸네일" />
      </div>
    </section>
  </div>
</template>

<style scoped>
.netflix-root {
  background: #141414;
  color: #fff;
  min-height: 100vh;
  font-family: 'Noto Sans KR', Arial, sans-serif;
}
.netflix-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 40px;
  background: linear-gradient(180deg, rgba(20,20,20,0.9) 60%, rgba(20,20,20,0));
}
.logo {
  height: 38px;
}
.nav {
  display: flex;
  gap: 24px;
  margin-left: 40px;
}
.nav a {
  color: #fff;
  text-decoration: none;
  font-weight: 500;
  font-size: 1.1rem;
}
.profile .avatar {
  width: 36px;
  border-radius: 4px;
}
.main-banner {
  position: relative;
  height: 420px;
  background: url('https://image.tmdb.org/t/p/original/9Gtg2DzBhmYamXBS1hKAhiwbBKS.jpg') center/cover no-repeat;
  display: flex;
  align-items: flex-end;
}
.banner-content {
  padding: 40px;
  background: linear-gradient(90deg, rgba(20,20,20,0.9) 60%, rgba(20,20,20,0));
}
.banner-content h1 {
  font-size: 2.5rem;
  margin-bottom: 12px;
}
.banner-content p {
  font-size: 1.2rem;
  margin-bottom: 20px;
}
.banner-buttons button {
  background: #fff;
  color: #141414;
  border: none;
  padding: 10px 28px;
  margin-right: 12px;
  border-radius: 4px;
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.2s;
}
.banner-buttons button:last-child {
  background: rgba(109,109,110,0.7);
  color: #fff;
}
.content-section {
  padding: 32px 40px;
}
.content-section h2 {
  font-size: 1.5rem;
  margin-bottom: 18px;
}
.content-row {
  display: flex;
  gap: 16px;
  overflow-x: auto;
}
.content-thumb {
  width: 180px;
  height: 100px;
  object-fit: cover;
  border-radius: 4px;
  background: #222;
}
</style>
