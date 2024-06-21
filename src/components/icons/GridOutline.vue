<template>
  <svg xmlns="http://www.w3.org/2000/svg" :class="className" viewBox="0 0 512 512">
    <rect
      x="48"
      y="48"
      width="176"
      height="176"
      rx="20"
      ry="20"
      fill="none"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
      stroke-width="32"
    />
    <rect
      x="288"
      y="48"
      width="176"
      height="176"
      rx="20"
      ry="20"
      fill="none"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
      stroke-width="32"
    />
    <rect
      x="48"
      y="288"
      width="176"
      height="176"
      rx="20"
      ry="20"
      fill="none"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
      stroke-width="32"
    />
    <rect
      x="288"
      y="288"
      width="176"
      height="176"
      rx="20"
      ry="20"
      fill="none"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
      stroke-width="32"
    />
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "GridOutline",
  props: {
    className: {
      type: String,
      default: undefined,
    },
  },
});
</script>

<style scoped>
/* Add any additional styles if necessary */
</style>
