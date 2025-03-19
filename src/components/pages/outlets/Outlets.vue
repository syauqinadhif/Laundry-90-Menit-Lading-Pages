<!-- <template>
  <div class="pt-28 md:pt-32 pb-16 md:pb-32 max-w-screen-xl mx-auto">
    <div>
      <h2
        class="font-vagrounded font-black text-2xl md:text-4xl text-center text-gray-800"
      >
        OUTLET KAMI
      </h2>
      <div class="w-16 sm:w-32 h-1 bg-yellow-400 mt-4 mb-2 sm:mb-12 mx-auto"></div>
    </div>
    <div class="mx-4 sm:mx-0 mt-8 sm:mt-16 space-y-12">
      <div
        v-for="(outlet, i) in outlets"
        :key="i"
        :class="[
          'w-full sm:w-3/4 flex-col sm:flex-row flex rounded-2xl overflow-hidden drop-shadow-card3',
          i % 2 !== 0 ? 'ml-auto flex-row-reverse' : '',
        ]"
      >
        <div class="w-full sm:w-1/2 h-70 sm:h-80 py-4 px-4 bg-antiflashwhite">
          <div class="h-full">
            <img
              :alt="`Ilustrasi ${outlet.name}`"
              :src="outlet.image"
              class="h-64 w-full md:h-full rounded-xl"
            />
          </div>
        </div>
        <div class="w-auto sm:w-1 h-1 sm:h-auto bg-orange-400 px-1"></div>
        <div class="min-w-0 w-full py-4 md:py-12 px-6 md:px-10 bg-orange-200">
          <p
            class="font-vagrounded font-black ml-1 text-left text-xl md:text-3xl text-gray-800 mb-4 md:mb-6"
          >
            {{ outlet.name }}
          </p>
          <ul class="space-y-3 text-gray-800 text-lg">
            <li class="flex space-x-2">
              <i class="sm:mt-1 fas fa-map-marker-alt text-orange-500 ml-1"></i>
              <span class="text-sm md:text-base font-semibold">
                {{ outlet.address }}
              </span>
            </li>
            <li class="flex items-center space-x-2">
              <i class="fas fa-phone-alt text-orange-500"></i>
              <span class="text-sm md:text-base font-semibold">{{ outlet.phone }}</span>
            </li>
            <li class="flex items-center space-x-2">
              <i class="fas fa-clock text-orange-500"></i>
              <span class="text-sm md:text-base font-semibold">{{ outlet.hours }}</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import outletGitoGati from "@/assets/images/our-outlets-gitogati.jpeg";
import outletHaryadi from "@/assets/images/our-outlets-haryadi.jpg";
import outletPurwomartani from "@/assets/images/our-outlets-purwomartani.jpg";
import outletUII from "@/assets/images/our-outlets-UII.jpg";
import outletDamai from "@/assets/images/our-outlets-Damai.png";

export default defineComponent({
  data() {
    return {
      outlets: [
        {
          name: "Laundry 90 Menit Gito Gati",
          address:
            "Jl. Gito Gati ruko No.1, Penen, Donoharjo, Kec. Ngaglik, Kabupaten Sleman, Daerah Istimewa Yogyakarta 55581",
          phone: "0822-2094-3340",
          hours: "07:00 - 22:00",
          image: outletGitoGati,
        },
        {
          name: "Laundry 90 Menit Purwomartani",
          address:
            "Sebelah Bank BPD, Jl. Purwomartani No.12, Bromonilan, Purwomartani, Kec. Kalasan, Kabupaten Sleman, Daerah Istimewa Yogyakarta 55571",
          phone: "0815-6558-744",
          hours: "07:00 - 22:00",
          image: outletPurwomartani,
        },
        {
          name: "Laundry 90 Menit Haryadi",
          address:
            "Jl. Kapten Haryadi No.60, Lojajar, Sinduharjo, Kec. Ngaglik, Kabupaten Sleman, Daerah Istimewa Yogyakarta 55581",
          phone: "0882-2164-4519",
          hours: "07:00 - 22:00",
          image: outletHaryadi,
        },
        {
          name: "Laundry 90 Menit Sehari hari UII",
          address:
            "Jl. Besi Jaya Jl. Kaliurang No.km 13, Besi, Sukoharjo, Kec. Ngaglik, Kabupaten Sleman, Daerah Istimewa Yogyakarta 55581",
          phone: "0823-3145-8745",
          hours: "08:00 - 21:00",
          image: outletUII,
        },
        {
          name: "Laundry 90 Menit Damai",
          address:
            "Jl. Damai No.5, Tambakan, Sinduharjo, Kec. Ngaglik, Kabupaten Sleman, Daerah Istimewa Yogyakarta 55581",
          phone: "0823-3145-8745",
          hours: "07:00 - 22:00",
          image: outletDamai,
        },
      ],
    };
  },
});
</script>

<style scoped>
.bg-antiflashwhite {
  background-color: #f2f2f2;
}
.bg-azureishwhite2 {
  background-color: #e5e7eb;
}
.text-richblack {
  color: #111827;
}
.text-darkgunmetal {
  color: #374151;
}
.drop-shadow-card3 {
  --tw-drop-shadow: drop-shadow(0 4px 6px rgba(0, 0, 0, 0.1));
  filter: var(--tw-drop-shadow);
}
</style> -->
<template>
  <div
    class="max-w-screen-xl flex flex-col lg:flex-row max-w-7xl mx-auto pt-40 pb-40 px-6 space-y-8 lg:space-y-0 lg:space-x-8 font-vagrounded text-center lg:text-left">
    <!-- Left Side Text -->
    <div class="w-full lg:w-1/2 mb-6 lg:mb-0 px-4">
      <h2 class="text-base font-vagrounded tracking-wider text-primaryblue uppercase mb-2">
        ONE CLICK LAUNDRY
      </h2>
      <h1 class="text-3xl md:text-4xl font-bold text-black leading-tight mb-4">
        Laundry Express Antar-Jemput Seluruh Yogyakarta
      </h1>
      <p class="text-sm md:text-base text-gray-600 mb-4">
        Kami siap membantu Anda dengan layanan laundry cepat, bersih, dan nyaman.
        Hubungi kami untuk layanan terbaik di daerah Anda.
      </p>
      <div class="mt-6 text-gray-700">
        <div class="flex flex-col sm:flex-row items-center sm:items-start mb-4">
          <img src="@/assets/images/email-2.png" alt="Email" class="w-6 h-6 text-orange-500 mr-3" />
          <a class="text-sm break-all">
            one1.click.laundry@gmail.com
          </a>
        </div>
        <div class="flex flex-col sm:flex-row items-center sm:items-start mb-4">
          <img src="@/assets/images/phone-2.png" alt="Phone" class="w-6 h-6 text-orange-500 mr-3" />
          <a class="text-sm">
            082325643594
          </a>
        </div>
        <div class="flex flex-col sm:flex-row items-center sm:items-start">
          <img src="@/assets/images/location-2.png" alt="Location" class="w-6 h-6 text-orange-500 mr-3" />
          <span class="text-sm">
            Jl. Gito Gati ruko No.1, Penen, Donoharjo, Ngaglik, Sleman, 55581
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({});
</script>

<style scoped>
.font-productsans {
  font-family: 'Product Sans', sans-serif;
}
</style>
