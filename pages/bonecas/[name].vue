<template>
  <section>
    <h2 class="main__h2 main__h2--bold">{{ boneca?.title }}</h2>
    <p class="main__p main__p--small">{{ boneca?.description }}</p>
    <Gallery v-if="boneca?.images" :images="boneca?.images" />
  </section>
</template>

<script setup>
import { ref } from "vue";
import bonecas from "../data/bonecas.json";

const route = useRoute();
const name = route?.params?.name.toUpperCase();
const boneca = ref(bonecas.items.find((item) => item.title === name));
</script>

<style scoped></style>
