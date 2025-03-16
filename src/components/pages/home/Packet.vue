<template>
  <div class="w-full bg-gray-100 flex flex-col items-center pt-8 md:pt-16 pb-16">
    <h2
      class="text-2xl md:text-4xl w-full md:w-1/2 font-vagrounded font-black text-gray-800 mb-4 text-center"
    >
      Paket <span class="text-orange-500">Laundry</span>
    </h2>

    <!-- Container Grid -->
    <div class="grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-4 gap-6 mt-6 px-4">
      <div
        v-for="(paket, index) in paketLaundry"
        :key="index"
        class="bg-white p-6 rounded-2xl shadow-md flex flex-col justify-between w-72"
        data-aos-duration="1000"
        data-aos="zoom-in"
      >
        <h3 class="text-lg text-center font-bold text-orange-500 mb-2">
          {{ paket.nama }}
        </h3>
        <ul class="text-gray-700 mb-4 space-y-2">
          <li
            v-for="(layanan, i) in paket.layanan"
            :key="i"
            class="flex items-center space-x-2"
          >
            <!-- SVG Centang -->
            <svg
              class="w-5 h-5 text-green-500"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path d="M5 13l4 4L19 7" />
            </svg>
            <span>{{ layanan }}</span>
          </li>
        </ul>
        <div class="flex justify-end">
          <button
            @click="redirectToWhatsApp(paket.nama, paket.harga)"
            class="bg-orange-500 text-white py-2 px-4 rounded-lg font-bold"
          >
            {{ paket.harga }}
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      nomorWA: "+6282325643594", // Nomor WhatsApp tujuan (tanpa spasi dan pakai kode negara)
      paketLaundry: [
        {
          nama: "Laundry Reguler Delivery",
          layanan: [
            "Layanan 24 Jam Selesai",
            "Layanan Antar Jemput Gratis 2 km",
            "Pakaian Sudah di Setrika",
            "Satu Customer, Satu Mesin Cuci",
          ],
          harga: "Rp. 10.000/kg",
        },
        {
          nama: "Laundry Express 12 Jam",
          layanan: [
            "Layanan 12 Jam Selesai",
            "Layanan Antar Jemput Gratis 2 km",
            "Pakaian Sudah di Setrika",
            "Satu Customer, Satu Mesin Cuci",
          ],
          harga: "Rp. 14.000/kg",
        },
        {
          nama: "Laundry Express 6 Jam",
          layanan: [
            "Layanan 6 Jam Selesai",
            "Layanan Antar Jemput Gratis 2 km",
            "Pakaian Sudah di Setrika",
            "Satu Customer, Satu Mesin Cuci",
          ],
          harga: "Rp. 17.000/kg",
        },
        {
          nama: "Laundry Express 3 Jam",
          layanan: [
            "Layanan 3 Jam Selesai",
            "Layanan Antar Jemput Gratis 2 km",
            "Pakaian Sudah di Setrika",
            "Satu Customer, Satu Mesin Cuci",
          ],
          harga: "Rp. 27.000/kg",
        },
      ],
    };
  },
  methods: {
    redirectToWhatsApp(namaPaket: string, hargaPaket: string) {
      const pesan = encodeURIComponent(
        `Halo, saya tertarik dengan paket *${namaPaket}* seharga *${hargaPaket}*. Bisa saya dapatkan informasi lebih lanjut?`
      );
      const url = `https://wa.me/${this.nomorWA}?text=${pesan}`;
      window.open(url, "_blank"); // Buka di tab baru
    },
  },
});
</script>
