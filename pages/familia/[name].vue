<template>
  <section>
    <h2 class="main__h2">{{ item?.title }}</h2>
    <p class="main__p">{{ item?.description }}</p>
    <Gallery v-if="item?.images" :images="item?.images" />
  </section>
</template>

<script setup>
import { ref } from "vue";
import familia from "../data/familia.json";

const route = useRoute();
const name = route?.params?.name;
const item = ref(familia.items.find((item) => item.link === name));
</script>

<style scoped></style>
