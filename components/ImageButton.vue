<template>
  <button :class="`image-button image-button--${id}`">
    <img
      class="image-button__img"
      :src="`./assets/buttons/${src}`"
      :alt="alt"
    />
  </button>
</template>
<script setup>
defineProps({
  id: { type: String, default: "" },
  src: { type: String, default: "" },
  alt: { type: String, default: "" },
});
</script>
<style scoped>
.image-button {
  background: transparent;
  border: 0;
  cursor: pointer;
}

.image-button__img {
  width: 100%;
}

@media (min-width: 1024px) {
  .image-button {
    position: absolute;
  }

  .image-button--cecilia {
    left: -32px;
    top: -64px;
  }

  .image-button--rafaela {
    left: 470px;
    top: 170px;
  }
}
</style>
