<script setup>
import Banner from './components/Banner.vue'
import MovieRow from './components/MovieRow.vue'

const trending = [
  { title: '오징어 게임', image: 'https://image.tmdb.org/t/p/w500/5P8SmMzSNYikXpxil6BYzJ16611.jpg' },
  { title: '더 글로리', image: 'https://image.tmdb.org/t/p/w500/9Gtg2DzBhmYamXBS1hKAhiwbBKS.jpg' },
  { title: '킹덤', image: 'https://image.tmdb.org/t/p/w500/6EdKBYkB1ssgGjc249ud1L55o8d.jpg' },
  { title: '지옥', image: 'https://image.tmdb.org/t/p/w500/8UlWHLMpgZm9bx6QYh0NFoq67TZ.jpg' },
]
const myList = [
  { title: '기묘한 이야기', image: 'https://image.tmdb.org/t/p/w500/x2LSRK2Cm7MZhjluni1msVJ3wDF.jpg' },
  { title: '브리저튼', image: 'https://image.tmdb.org/t/p/w500/4gKyQ1mcHa8ZKDsYoyKQSevF01J.jpg' },
  { title: '종이의 집', image: 'https://image.tmdb.org/t/p/w500/6aUWe0GSl69wMTSWWexsorMIvwU.jpg' },
  { title: '나르코스', image: 'https://image.tmdb.org/t/p/w500/7WsyChQLEftFiDOVTGkv3hFpyyt.jpg' },
]
</script>

<template>
  <div class="app">
    <header class="header">
      <img class="logo" src="https://upload.wikimedia.org/wikipedia/commons/7/7a/Logonetflix.png" alt="Netflix Logo" />
      <nav class="nav">
        <a href="#">홈</a>
        <a href="#">시리즈</a>
        <a href="#">영화</a>
        <a href="#">내 리스트</a>
      </nav>
    </header>
    <Banner />
    <MovieRow :title="'지금 뜨는 콘텐츠'" :movies="trending" />
    <MovieRow :title="'내 리스트'" :movies="myList" />
  </div>
</template>

<style scoped>
.app {
  background: #141414;
  min-height: 100vh;
  color: #fff;
}
.header {
  display: flex;
  align-items: center;
  padding: 20px 40px;
  background: linear-gradient(180deg, rgba(20,20,20,0.9) 60%, rgba(20,20,20,0));
  position: sticky;
  top: 0;
  z-index: 10;
}
.logo {
  height: 38px;
  margin-right: 40px;
}
.nav a {
  color: #fff;
  margin-right: 24px;
  text-decoration: none;
  font-weight: 500;
  font-size: 1.1rem;
}
.nav a:hover {
  text-decoration: underline;
}
</style>
