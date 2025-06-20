<script setup>
// 넷플릭스 메인 구조에 필요한 추가 로직이 있다면 여기에 작성
</script>

<template>
  <div class="netflix-app">
    <header class="netflix-header">
      <img src="https://assets.brand.microsites.netflix.io/assets/2d2e6b2e-7e2e-11e9-8f3b-066b49664af6_cm_800w.png?v=36" alt="Netflix Logo" class="netflix-logo" />
      <input type="text" placeholder="검색" class="search-bar" />
    </header>
    <main>
      <h2 class="section-title">인기 콘텐츠</h2>
      <div class="thumbnail-grid">
        <div v-for="n in 12" :key="n" class="thumbnail">
          <img :src="`https://picsum.photos/200/300?random=${n}`" alt="썸네일" />
        </div>
      </div>
    </main>
  </div>
</template>

<style scoped>
.netflix-app {
  background: #141414;
  min-height: 100vh;
  color: #fff;
  font-family: 'Noto Sans KR', Arial, sans-serif;
}
.netflix-header {
  display: flex;
  align-items: center;
  padding: 24px 32px 16px 32px;
  background: rgba(20, 20, 20, 0.95);
}
.netflix-logo {
  height: 40px;
  margin-right: 32px;
}
.search-bar {
  flex: 1;
  max-width: 320px;
  padding: 8px 16px;
  border-radius: 4px;
  border: none;
  font-size: 16px;
}
.section-title {
  margin: 32px 0 16px 32px;
  font-size: 1.5rem;
  font-weight: bold;
}
.thumbnail-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
  gap: 24px;
  padding: 0 32px 32px 32px;
}
.thumbnail img {
  width: 100%;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.5);
  transition: transform 0.2s;
}
.thumbnail img:hover {
  transform: scale(1.05);
}
</style>
