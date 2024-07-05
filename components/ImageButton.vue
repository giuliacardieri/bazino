<template>
  <router-link :class="`image-button image-button--${id}`" :to="link">
    <img
      class="image-button__img"
      :src="`./assets/buttons/${src}`"
      :alt="alt"
    />
  </router-link>
</template>
<script setup>
defineProps({
  id: { type: String, default: "" },
  src: { type: String, default: "" },
  alt: { type: String, default: "" },
  link: { type: String, default: "/" },
});
</script>
<style scoped>
.image-button__img {
  width: 100%;
}

@media (min-width: 1024px) {
  .image-button {
    position: absolute;
    z-index: 2;
  }

  .image-button--cecilia {
    left: -32px;
    top: -23px;
    width: 500px;
  }

  .image-button--rafaela {
    left: 429px;
    top: 174px;
    width: 300px;
  }
}
</style>
