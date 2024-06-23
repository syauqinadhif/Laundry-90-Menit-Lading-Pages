<template>
  <div class="h-dvh">
    <img
      alt="Gambar latar bagian hero"
      :src="heroCoverImg"
      class="absolute -z-50 w-full h-dvh object-cover"
    />
    <div
      class="max-w-screen-xl h-screen mx-auto flex flex-col sm:flex-row items-center gap-x-12 overflow-hidden"
    >
      <div class="relative mx-4 md:mx-8">
        <h1
          class="mt-32 md:mt-24 font-vagrounded font-black text-gray-800 text-3xl leading-tight sm:text-5xl sm:leading-tight"
        >
          Laundry Express Antar-Jemput,
          <span class="text-orange-500"> Self Service, </span>
          <span class="text-yellow-500">Kiloan dan Satuan.</span>
        </h1>
        <p class="mt-2 text-sm sm:text-lg text-gray-800 font-productsans">
          Mau baju bersih dalam sekejap? Di Laundry 90 Menit, serahkan baju kotor, nonton
          satu episode serial kesukaanmu, dan voila! Baju udah siap balik ke lemari.
        </p>
        <a
          href="https://wa.me/+6282325643594"
          class="w-fit h-8 md:h-12 bg-orange-500 mt-4 md:mt-8 px-4 md:px-8 flex items-center justify-center text-center font-medium text-white text-xs md:text-sm rounded-3xl"
        >
          Laundry Sekarang!
        </a>
      </div>
      <img
        alt="Gambar Ilustrasi Hero"
        :src="heroImg"
        class="relative md:mt-16 w-80 sm:w-96 md:w-full pointer-events-none select-none"
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
