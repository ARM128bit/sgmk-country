<script setup lang="ts">
interface DefaultProps {
  active: boolean;
}
withDefaults(defineProps<DefaultProps>(), {
  active: false,
});
</script>
<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    height="24px"
    viewBox="0 0 24 24"
    width="24px"
    fill="#000000"
    class="favourite-icon"
    :class="{ 'favourite-icon--active': active }"
  >
    <path d="M0 0h24v24H0z" fill="none" />
    <path
      d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"
    />
  </svg>
</template>

<style scoped lang="scss">
.favourite-icon {
  cursor: pointer;
  fill: var(--color-text);
  transition: all 0.3s ease;

  &--active {
    fill: var(--vt-c-orange);
  }
  &:not(.favourite-icon--active):hover {
    fill: var(--vt-c-slate-gray);
  }
}
</style>
