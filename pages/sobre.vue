<template>
  <section class="image-text-group">
    <div class="image-text-group__text">
      <h2 class="main__h2">{{ sobre.title }}</h2>
      <p class="main__p" v-for="(item, i) in sobre.text" :key="i">{{ item }}</p>
    </div>
    <img class="image-text-group__image" src="" alt="Matheus Baz" />
  </section>
</template>

<script setup>
import sobre from "../data/sobre.json";
</script>

<style scoped>
.image-text-group {
  align-items: center;
  display: flex;
  gap: 48px;
}

.image-text-group__text {
  width: 40%;
}

.image-text-group__image {
  width: 60%;
}
</style>
