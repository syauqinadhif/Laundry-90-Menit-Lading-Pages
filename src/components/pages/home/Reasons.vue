<template>
  <div class="bg-cultured2 pt-16 md:pt-24 pb-14">
    <div class="max-w-screen-xl mx-auto">
      <h3
        class="font-mont font-black px-6 text-3xl sm:text-5xl text-left sm:text-center leading-tight"
      >
        <span class="text-gunmetal font-vagrounded">Mengapa</span>
        <span class="text-orange-500 font-vagrounded"> Laundry 90 Menit</span
        ><span class="text-gunmetal font-vagrounded"> ?</span>
      </h3>
      <p
        class="font-productsans mt-2 sm:mt-6 px-6 sm:px-32 md:px-44 lg:px-64 text-left sm:text-center text-gunmetal text-sm sm:text-lg"
      >
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
        incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
        exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </p>
      <div class="mt-8 md:mt-16 px-6 space-y-8">
        <div class="flex flex-col sm:flex-row items-center justify-between">
          <img
            alt="Gambar alasan pertama"
            :src="reason1Img"
            data-aos="fade-right"
            data-aos-duration="1000"
            class="pointer-events-none select-none h-80"
          />
          <div data-aos="fade-left" data-aos-duration="1000" class="max-w-xl">
            <p class="text-orange-500 text-3xl sm:text-4xl">
              <span class="font-productsans font-black">#</span
              ><span class="font-mont font-black">1</span>
              <span class="font-mont font-black">Laundry</span>
              <span class="font-mont">90Menit</span>
            </p>
            <p
              class="mt-2.5 font-mont font-black text-2xl sm:text-4xl text-gunmetal leading-tight"
            >
              Reasons Heading
            </p>
            <p class="mt-1.5 font-productsans sm:text-lg text-gunmetal">
              <!-- Bengkel Inovasi berpengalaman menangani berbagai proyek dari berbagai bidang
              <i>engineering</i> mulai dari <i>embedded system</i>,
              <i>microcontroller</i>, Internet of Things, pengembangan web, pengembangan
              aplikasi, dll. -->
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
              tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
              quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
              consequat.
            </p>
          </div>
        </div>
        <div class="flex flex-wrap items-center justify-between">
          <div
            data-aos="fade-right"
            data-aos-duration="1000"
            class="max-w-xl order-2 sm:order-1"
          >
            <p class="text-orange-500 text-3xl sm:text-4xl">
              <span class="font-productsans font-black">#</span
              ><span class="font-mont font-black">2</span>
              <span class="font-mont font-black">Laundry</span>
              <span class="font-mont">90Menit</span>
            </p>
            <p
              class="mt-2.5 font-mont font-black text-2xl sm:text-4xl text-gunmetal leading-tight"
            >
              Reasons Heading
            </p>
            <p class="mt-1.5 font-productsans sm:text-lg text-gunmetal">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
              tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
              quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
              consequat.
              <!-- Bengkel Inovasi memiliki teknisi yang berpengalaman di berbagai bidang
              <i>engineering</i>. -->
            </p>
          </div>
          <img
            alt="Gambar alasan kedua"
            :src="reason2Img"
            data-aos="fade-left"
            data-aos-duration="1000"
            class="pointer-events-none select-none order-1 sm:order-2 h-80"
          />
        </div>
        <div class="flex flex-col sm:flex-row items-center justify-between">
          <img
            alt="Gambar alasan ketiga"
            :src="reason3Img"
            data-aos="fade-right"
            data-aos-duration="1000"
            class="pointer-events-none select-none h-80"
          />
          <div data-aos="fade-left" data-aos-duration="1000" class="max-w-xl">
            <p class="text-orange-500 text-3xl sm:text-4xl">
              <span class="font-productsans font-black">#</span
              ><span class="font-mont font-black">3</span>
              <span class="font-mont font-black">Laundry</span>
              <span class="font-mont">90Menit</span>
            </p>
            <p
              class="mt-2.5 font-mont font-black text-2xl sm:text-4xl text-gunmetal leading-tight"
            >
              Reasons Heading
            </p>
            <p class="mt-1.5 font-productsans sm:text-lg text-gunmetal">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
              tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
              quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
              consequat.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import reason1Img from "@/assets/images/wash-and-fold.jpg";
import reason2Img from "@/assets/images/wash-and-fold.jpg";
import reason3Img from "@/assets/images/wash-and-fold.jpg";

export default {
  name: "ReasonsSection",
  data() {
    return {
      reason1Img,
      reason2Img,
      reason3Img,
    };
  },
};
</script>
