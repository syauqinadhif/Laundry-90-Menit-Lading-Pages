<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";
import { RouterView } from "vue-router";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import WhatsappCta from "./components/WhatsappCta.vue";

// Reactive reference to store scroll position
const scrollY = ref(0);

// Function to handle scroll event and update scrollY
const handleScroll = () => {
  scrollY.value = window.scrollY;
};

// Attach scroll event listener on mount and remove it on unmount
onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <Header :scrollY="scrollY" />
  <RouterView />
  <WhatsappCta />
  <Footer />
</template>

<style>
/* Add any global styles here if needed */
</style>
