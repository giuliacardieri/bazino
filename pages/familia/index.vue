<template>
  <section>
    <h2 class="main__h2">{{ familia?.title }}</h2>
    <p class="main__p" v-for="(item, i) in familia?.description" :key="i">
      {{ item }}
    </p>
    <div class="links">
      <router-link
        v-for="item in familia?.items"
        :key="item.link"
        :to="`/familia/${item.link}`"
        >{{ item.title }}</router-link
      >
    </div>
  </section>
</template>

<script setup>
import familia from "../data/familia.json";
</script>

<style scoped>
.links {
  display: flex;
  gap: 16px;
  margin-top: 32px;
}
</style>
