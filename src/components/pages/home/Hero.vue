<template>
  <div class="h-dvh relative">
    <img alt="Gambar latar bagian hero" :src="heroCoverImg" class="absolute -z-50 w-full h-full object-cover" />
    <div class="max-w-screen-xl h-full mx-auto flex flex-col md:flex-row items-center gap-x-4 gap-y-12 overflow-hidden">
      <div class="mx-4 md:mx-8 md:w-1/2">
        <h1
          class="mt-32 md:mt-24 font-vagrounded font-black text-gray-800 text-3xl leading-tight sm:text-5xl sm:leading-tight">
          Laundry Express
          <span class="text-primaryblue"> Antar-Jemput,</span>
          Nomor 1
          <!-- <span class="text-yellow-500">Kiloan dan Satuan.</span> -->
          <!-- <span class="text-primaryblue"> 1 </span> -->
          di Yogyakarta.
        </h1>
        <p class="mt-2 text-sm sm:text-lg text-gray-800 font-productsans">
          Mau baju bersih tanpa ganggu liburan? Pesan layanan One Click Laundry, kami jemput cucianmu, anda lanjutkan
          liburan anda dan dalam waktu singkat baju siap kembali. Praktis, cepat, dan tanpa repot!
        </p>
        <p class="md:hidden mt-8 mb-8 text-sm sm:text-lg text-gray-800 font-light">
          *Coming Soon! OneClickLaundry App will be available on Play Store and App Store.
        </p>
        <a 
        href="https://wa.me/+6282264206100?text=Halo,%20saya%20tertarik%20mengetahui%20lebih%20lanjut%20layanan%20One%20Click%20Laundry.%20Bisa%20saya%20dapatkan%20informasi%20lebih%20lanjut?"
          class="w-fit h-8 md:h-12 bg-primaryblue mt-4 md:mt-8 px-4 md:px-8 flex items-center justify-center text-center font-medium text-white text-xs md:text-sm rounded-3xl">
          Laundry Sekarang!
        </a>
        <p class="hidden md:block mt-32 text-sm sm:text-lg text-gray-800 font-light">
          *Coming Soon! OneClickLaundry App will be available on Play Store and App Store.
        </p>
      </div>
      <div class="w-1/2 mx-8">
        <img alt="Gambar Ilustrasi Hero" :src="heroImg"
          class="absolute bottom-0 right-2 sm:right-16 md:w-1/2 xl:w-2/5 max-h-[50%] md:max-h-[100%] pointer-events-none select-none" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import heroCoverImg from "@/assets/images/home-hero-cover-2.png";
// import heroImg from "@/assets/images/illustration-hero-2.png";
import heroImg from "@/assets/images/hero-baru.png";

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
