<template>
  <div class="w-full bg-gray-100 flex flex-col items-center pt-8 md:pt-16 pb-16">
    <h2
      class="text-2xl md:text-4xl w-full md:w-1/2 font-vagrounded font-black text-gray-800 mb-4 text-center"
    >
      Kami Hadir Untuk Membuat
      <span class="text-orange-500">Pelanggan</span>
      Kami
      <span class="text-orange-500">Tersenyum</span>
      Dengan
      <span class="text-orange-500">Layanan</span>
      Kami.
    </h2>
    <div class="mt-8 md:mt-16 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div
        v-for="service in services"
        :key="service.title"
        data-aos="zoom-in-up"
        data-aos-duration="1000"
        class="relative rounded-lg overflow-hidden"
      >
        <div class="bg-gray-100 h-80">
          <img
            :src="service.image"
            :alt="service.title"
            class="w-64 h-64 object-cover rounded-lg"
          />
          <div class="absolute mx-4 bottom-0 left-0 right-0 p-4 bg-blue-100 rounded-lg">
            <div class="flex items-center">
              <img :src="service.icon" :alt="service.title" class="w-6 h-6 mr-2" />
              <h3 class="text-lg font-semibold text-gray-800">{{ service.title }}</h3>
            </div>
            <p class="text-orange-500 mt-2">
              <a href="/layananKami" class="hover:underline">View Details →</a>
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import selfServices from "@/assets/images/self-service.jpg";
import selfServicesIcon from "@/assets/images/self-service.png";
import laundryKiloan from "@/assets/images/kiloan-reguler.jpg";
import laundryKiloanIcon from "@/assets/images/laundry-kiloan.png";
import laundrySatuan from "@/assets/images/satuan-premium.jpg";
import laundrySatuanIcon from "@/assets/images/laundry-satuan.png";
import laundrySepatuDanTas from "@/assets/images/tas-dan-sepatu.jpg";
import laundrySepatuDanTasIcon from "@/assets/images/laundry-tas-dan-sepatu.png";
import laundryPerkapBayi from "@/assets/images/perkap-bayi.jpg";
import laundryPerkapBayiIcon from "@/assets/images/laundry-baby-equipment.png";
import laundryChemical from "@/assets/images/chemical.jpg";
import laundryChemicalIcon from "@/assets/images/laundry-chemical.png";
// import WashAndFoldIcon from "@/assets/wash_and_fold_icon.png";
// import DryCleaningIcon from "@/assets/dry_cleaning_icon.png";
// import IronClothesIcon from "@/assets/iron_clothes_icon.png";
// import StainRemovalIcon from "@/assets/stain_removal_icon.png";
// import ClotheSewingIcon from "@/assets/clothe_sewing_icon.png";
// import BeddingCleaningIcon from "@/assets/bedding_cleaning_icon.png";

export default defineComponent({
  data() {
    return {
      services: [
        {
          title: "Self Services",
          image: selfServices,
          icon: selfServicesIcon,
        },
        {
          title: "Kiloan Reguler",
          image: laundryKiloan,
          icon: laundryKiloanIcon,
        },
        {
          title: "Satuan Premium",
          image: laundrySatuan,
          icon: laundrySatuanIcon,
        },
        {
          title: "Sepatu dan Tas",
          image: laundrySepatuDanTas,
          icon: laundrySepatuDanTasIcon,
        },
        {
          title: "Peralatan Bayi",
          image: laundryPerkapBayi,
          icon: laundryPerkapBayiIcon,
        },
        {
          title: "Chemical",
          image: laundryChemical,
          icon: laundryChemicalIcon,
        },
      ],
    };
  },
});
</script>
