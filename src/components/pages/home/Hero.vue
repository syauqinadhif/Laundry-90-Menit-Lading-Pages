<template>
  <div class="h-dvh">
    <img
      alt="Gambar latar bagian hero"
      :src="heroCoverImg"
      class="absolute -z-50 w-full h-dvh object-cover"
    />
    <div
      class="max-w-screen-xl h-screen mx-auto flex items-center gap-x-64 overflow-hidden"
    >
      <div class="relative">
        <h1 class="mt-8 font-vagrounded text-darkgunmetal text-xl sm:text-5xl">
          Laundry Express Antar-Jemput Self Service, Kiloan dan Satuan.
        </h1>
        <p class="mt-2 text-base sm:text-lg text-darkgunmetal">
          Solusi Cepat Untuk Bantu Nyuciin Cucian Kotor Kamu!
        </p>
        <a
          href="/"
          class="w-fit h-12 bg-orange-500 mt-8 px-8 flex items-center justify-center text-center font-medium text-white text-sm rounded-3xl"
        >
          Laundry Sekarang!
        </a>
      </div>
      <img
        alt="Gambar Ilustrasi Hero"
        class="relative w-96 pointer-events-none select-none"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import heroCoverImg from "@/assets/images/home-hero-cover.png";
import heroImg from "@/assets/images/illustration-hero.png";

export default defineComponent({
  data() {
    return {
      heroCoverImg,
      heroImg,
    };
  },
});
</script>
