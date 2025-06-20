<template>
  <section class="banner">
    <img class="banner-bg" :src="banner.image" alt="banner" />
    <div class="banner-content">
      <h1 class="banner-title">{{ banner.title }}</h1>
      <p class="banner-desc">{{ banner.desc }}</p>
      <div class="banner-buttons">
        <button class="play">▶ 재생</button>
        <button class="info">상세 정보</button>
      </div>
    </div>
    <div class="banner-fade"></div>
  </section>
</template>

<script setup>
const banner = {
  title: '오징어 게임',
  desc: '456억의 상금이 걸린 의문의 서바이벌 게임에 참가한 사람들의 이야기. 단 한 명만이 살아남는다!',
  image: 'https://image.tmdb.org/t/p/original/5P8SmMzSNYikXpxil6BYzJ16611.jpg',
}
</script>

<style scoped>
.banner {
  position: relative;
  height: 420px;
  color: #fff;
  display: flex;
  align-items: flex-end;
  overflow: hidden;
  margin-bottom: 32px;
}
.banner-bg {
  position: absolute;
  top: 0; left: 0; width: 100%; height: 100%; object-fit: cover;
  z-index: 1;
  filter: brightness(0.6);
}
.banner-content {
  position: relative;
  z-index: 2;
  margin: 0 0 60px 40px;
}
.banner-title {
  font-size: 2.8rem;
  font-weight: bold;
  margin-bottom: 16px;
}
.banner-desc {
  font-size: 1.2rem;
  width: 40vw;
  margin-bottom: 24px;
}
.banner-buttons button {
  background: rgba(51,51,51,0.7);
  border: none;
  color: #fff;
  padding: 10px 28px;
  margin-right: 12px;
  font-size: 1.1rem;
  border-radius: 4px;
  cursor: pointer;
  font-weight: 500;
  transition: background 0.2s;
}
.banner-buttons .play {
  background: #fff;
  color: #000;
}
.banner-buttons button:hover {
  background: #e6e6e6;
  color: #000;
}
.banner-fade {
  position: absolute;
  bottom: 0; left: 0; width: 100%; height: 120px;
  background: linear-gradient(180deg, transparent, #141414 90%);
  z-index: 3;
}
</style> 