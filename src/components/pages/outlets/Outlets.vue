<template>
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
</style>
