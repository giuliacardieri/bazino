<template>
  <div class="icon-text-group">
    <img class="icon-text-group__icon" :src="`/assets/icons/${icon}.svg`" />
    <h3 class="icon-text-group__text"><slot></slot></h3>
  </div>
</template>
<script setup>
defineProps({
  icon: { type: String, default: "" },
});
</script>
<style scoped>
.icon-text-group {
  align-items: center;
  display: flex;
  gap: 8px;
}

.icon-text-group__text :deep(a) {
  color: var(--black);
  font-size: 16px;
  text-decoration: none;
}
</style>
