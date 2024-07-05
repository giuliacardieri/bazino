<template>
  <div class="gallery">
    <img
      v-for="image in images"
      :key="image.src"
      class="gallery__image"
      :src="`/assets/${image?.src}`"
      :alt="image?.alt"
    />
  </div>
</template>
<script setup>
defineProps({
  images: { type: Array, default: [] },
});
</script>
<style scoped>
.gallery {
  display: grid;
  gap: 32px;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  margin-top: 32px;
}

@media (max-width: 1023px) {
  .gallery {
    gap: 16px;
    grid-template-columns: minmax(0, 1fr);
  }
}

.gallery__image {
  width: 100%;
}
</style>
