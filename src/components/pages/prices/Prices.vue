<template>
  <div class="max-w-screen-xl mx-auto py-32 p-4">
    <h1
      class="text-center text-2xl lg:text-4xl font-bold mb-2 font-vagrounded text-gray-800"
    >
      FULL SERVICES
    </h1>
    <div class="w-24 lg:w-48 h-1 bg-yellow-400 mt-4 mb-6 lg:mb-12 mx-auto"></div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div
        v-for="(service, index) in services"
        :key="index"
        class="relative bg-softgray rounded-2xl shadow-lg p-6"
      >
        <h2 class="text-xl font-vagrounded text-orange-500 mb-4">{{ service.name }}</h2>
        <ul class="mb-16">
          <li
            v-for="(price, subIndex) in service.prices"
            :key="subIndex"
            class="flex justify-between items-center mb-2"
          >
            <span class="flex items-center font-productsans">
              <span class="w-2.5 h-2.5 bg-orange-500 rounded-full mr-2"></span>
              {{ price.type }}
            </span>
            <span class="font-productsans">{{ price.cost }}</span>
          </li>
        </ul>
        <button
          class="absolute bottom-4 right-4 bg-orange-500 text-white py-2 px-4 rounded-3xl hover:bg-orange-600"
        >
          Order
        </button>
      </div>
    </div>
    <div class="flex flex-col sm:flex-row justify-center gap-6 mt-6">
      <div
        v-for="(service, index) in extraFullServices"
        :key="index"
        class="relative bg-softgray rounded-2xl shadow-lg p-6 w-full max-w-sm"
      >
        <h2 class="text-xl font-vagrounded text-orange-500 mb-4">{{ service.name }}</h2>
        <ul class="mb-16">
          <li
            v-for="(price, subIndex) in service.prices"
            :key="subIndex"
            class="flex justify-between items-center mb-2"
          >
            <span class="flex items-center">
              <span class="w-2.5 h-2.5 bg-orange-500 rounded-full mr-2"></span>
              {{ price.type }}
            </span>
            <span>{{ price.cost }}</span>
          </li>
        </ul>
        <button
          class="absolute bottom-4 right-4 bg-orange-500 text-white py-2 px-4 rounded-3xl hover:bg-orange-600"
        >
          Order
        </button>
      </div>
    </div>
    <h1
      class="text-center text-2xl lg:text-4xl font-bold mt-16 mb-2 font-vagrounded text-gray-800"
    >
      SELF SERVICES
    </h1>
    <div class="w-24 lg:w-44 h-1 bg-yellow-400 mt-4 mb-6 lg:mb-12 mx-auto"></div>
    <div class="flex flex-col sm:flex-row justify-center gap-6 mt-6">
      <div
        v-for="(service, index) in selfServices"
        :key="index"
        class="relative bg-softgray rounded-2xl shadow-lg p-6 w-full h-fit max-w-sm"
      >
        <h2 class="text-xl font-vagrounded text-orange-500 mb-4">{{ service.name }}</h2>
        <ul class="mb-16">
          <li
            v-for="(price, subIndex) in service.prices"
            :key="subIndex"
            class="flex justify-between items-center mb-2"
          >
            <span class="flex items-center">
              <span class="w-2.5 h-2.5 bg-orange-500 rounded-full mr-2"></span>
              {{ price.type }}
            </span>
            <span>{{ price.cost }}</span>
          </li>
        </ul>
        <!-- <button
          class="absolute bottom-4 right-4 bg-orange-500 text-white py-2 px-4 rounded-3xl hover:bg-orange-600"
        >
          Order
        </button> -->
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

interface Price {
  type: string;
  cost: string;
}

interface Service {
  name: string;
  prices: Price[];
}

export default defineComponent({
  name: "FullService",
  data() {
    return {
      services: [
        {
          name: "Cuci Setrika/kg",
          prices: [
            { type: "1 Hari", cost: "Rp8.000" },
            { type: "2 Hari", cost: "Rp7.000" },
            { type: "12 Jam", cost: "Rp12.000" },
            { type: "6 Jam", cost: "Rp15.000" },
          ],
        },
        {
          name: "Cuci Lipat/kg",
          prices: [
            { type: "1 Hari", cost: "Rp5.000" },
            { type: "12 Jam", cost: "Rp7.000" },
            { type: "6 Jam", cost: "Rp10.000" },
            { type: "3 Jam", cost: "Rp15.000" },
          ],
        },
        {
          name: "Bed Cover",
          prices: [
            { type: "Ukuran Kecil", cost: "Rp20.000" },
            { type: "Ukuran Sedang", cost: "Rp25.000" },
            { type: "Ukuran Besar", cost: "Rp30.000" },
            { type: "Super Besar", cost: "Rp45.000" },
          ],
        },
      ] as Service[],
      extraFullServices: [
        {
          name: "Satuan",
          prices: [
            { type: "Blazer / Batik", cost: "Rp35.000" },
            { type: "Gamis / Tunik", cost: "Rp30.000" },
            { type: "Boneka S", cost: "Rp30.000" },
            { type: "Bantal", cost: "Rp25.000" },
          ],
        },
        {
          name: "Setrika/kg",
          prices: [
            { type: "1 Hari", cost: "Rp8.000" },
            { type: "2 Hari", cost: "Rp7.000" },
          ],
        },
      ] as Service[],
      selfServices: [
        {
          name: "Outlet Gito-Gati dan Haryadi",
          prices: [
            { type: "Cuci Saja", cost: "Rp12.000" },
            { type: "Keringkan", cost: "Rp15.000" },
            { type: "Cuci Kering", cost: "Rp27.000" },
          ],
        },
        {
          name: "Outlet Purwomartani",
          prices: [
            { type: "Cuci Saja", cost: "Rp10.000" },
            { type: "Keringkan", cost: "Rp15.000" },
            { type: "Cuci Kering", cost: "Rp25.000" },
          ],
        },
      ] as Service[],
    };
  },
});
</script>
