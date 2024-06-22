<template>
  <div
    class="h-full w-full bg-gray-100 px-4 md:px-0 pt-8 md:pt-16 pb-24 flex flex-col items-center"
  >
    <div class="max-w-screen-xl mx-auto">
      <div class="flex justify-between items-center text-center mb-8">
        <h2
          class="text-2xl md:text-3xl text-center md:text-left font-vagrounded text-gray-800"
        >
          Kunjungi<span class="text-orange-500"> Outlet</span> Kami
        </h2>
      </div>
      <div class="mt-6 md:mt-12 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div
          v-for="news in newsList"
          :key="news.title"
          class="bg-white rounded-lg shadow-lg overflow-hidden"
          data-aos-duration="1000"
          data-aos="zoom-in"
        >
          <div class="mt-4 mx-4 text-left">
            <div class="flex justify-between text-sm text-gray-600 mb-2">
              <!-- <span>{{ news.date }}</span> -->
              <h1 class="text-softred font-bold">{{ news.outletNumber }}</h1>
            </div>
            <!-- <div class="text-orange-500 text-xs mb-2">Details</div> -->
          </div>

          <div class="h-44 mx-4">
            <img :src="news.image" :alt="news.title" class="w-full h-full rounded-lg" />
          </div>
          <div class="p-4">
            <a
              href="/"
              class="relative w-8 h-12 z-10 py-1 px-3 bg-white hover:bg-softred border-softred border-2 font-medium text-softred hover:text-white text-xs rounded-3xl"
            >
              Details
            </a>
            <h3 class="pt-4 text-lg font-vagrounded text-gray-800">{{ news.title }}</h3>
          </div>
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
      newsList: [
        {
          outletNumber: "#1 Outlet",
          readTime: "2 Min Read",
          title: "Outlet Laundry 90 Menit Gito Gati",
          image: outletGitoGati,
        },
        {
          outletNumber: "#2 Outlet",
          readTime: "8 Min Read",
          title: "Outlet Laundry 90 Menit Haryadi",
          image: outletHaryadi,
        },
        {
          outletNumber: "#3 Outlet",
          readTime: "6 Min Read",
          title: "Outlet Laundry 90 Menit Purwomartani",
          image: outletPurwomartani,
        },
        {
          outletNumber: "#4 Outlet",
          readTime: "6 Min Read",
          title: "Outlet Laundry Sehari-hari UII",
          image: outletUII,
        },
        // Add more news items here
      ],
    };
  },
});
</script>
