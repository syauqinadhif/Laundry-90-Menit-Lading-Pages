<template>
  <Hero />
  <Testimonials />
  <Packet />
  <!-- <Services /> -->
  <Reasons />
  <Outlets />
</template>

<script lang="ts">
import Hero from "@/components/pages/home/Hero.vue";
import Testimonials from "@/components/pages/home/Testimonials.vue";
// import Services from "@/components/pages/home/Services.vue";
import Packet from "@/components/pages/home/Packet.vue";
import Reasons from "@/components/pages/home/Reasons.vue";
import Outlets from "@/components/pages/home/Outlets.vue";

export default {
  components: {
    Hero,
    Testimonials,
    Packet,
    // Services,
    Reasons,
    // Outlets,
  },
};
</script>
