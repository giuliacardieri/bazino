<template>
  <section>
    <h2 class="main__h2 main__h2--bold">{{ item?.title }}</h2>
    <p class="main__p main__p--small">{{ item?.description }}</p>
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
