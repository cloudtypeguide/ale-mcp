<script setup>
const props = defineProps({
  title: String,
  movies: Array,
})
</script>

<template>
  <section class="row">
    <h2 class="row-title">{{ title }}</h2>
    <div class="row-posters">
      <div v-for="movie in movies" :key="movie.title" class="row-poster">
        <img :src="movie.image" :alt="movie.title" />
        <div class="row-movie-title">{{ movie.title }}</div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.row {
  margin-left: 40px;
  margin-bottom: 36px;
}
.row-title {
  font-size: 1.4rem;
  font-weight: 600;
  margin-bottom: 12px;
}
.row-posters {
  display: flex;
  overflow-x: auto;
  padding-bottom: 8px;
}
.row-poster {
  margin-right: 18px;
  flex: 0 0 auto;
  width: 160px;
  cursor: pointer;
  transition: transform 0.2s;
}
.row-poster img {
  width: 100%;
  border-radius: 6px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.4);
  margin-bottom: 6px;
}
.row-poster:hover {
  transform: scale(1.08);
  z-index: 2;
}
.row-movie-title {
  font-size: 1rem;
  text-align: center;
  color: #eee;
}
</style> 