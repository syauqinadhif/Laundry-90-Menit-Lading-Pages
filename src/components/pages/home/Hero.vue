<template>
  <div class="h-dvh relative">
    <img
      alt="Gambar latar bagian hero"
      :src="heroCoverImg"
      class="absolute -z-50 w-full h-full object-cover"
    />
    <div
      class="max-w-screen-xl h-full mx-auto flex flex-col md:flex-row items-center gap-x-4 gap-y-12 overflow-hidden"
    >
      <div class="mx-4 md:mx-8 md:w-1/2 z-10">
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
      <div class="w-1/2 mx-8">
        <img
          alt="Gambar Ilustrasi Hero"
          :src="heroImg"
          class="absolute bottom-0 right-2 sm:right-16 w- sm:w-1/4 max-h-[50%] md:max-h-[100%] pointer-events-none select-none"
        />
      </div>
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

<style scoped>
/* Tambahkan padding-bottom agar gambar tidak menutupi konten lain */
.relative.w-full.md\:w-1\/2.flex.justify-end.items-end {
  padding-bottom: 0;
}
</style>
