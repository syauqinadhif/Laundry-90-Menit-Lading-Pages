<template>
  <div>
    <!-- Chat Button -->
    <div class="fixed bottom-4 right-4 flex items-center -z-100">
      <button
        @click="togglePopup"
        class="px-4 py-2 bg-white rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300"
      >
        <span>Butuh bantuan? Chat saja.</span>
      </button>
      <img
        v-if="!showPopup"
        @click="togglePopup"
        src="@/assets/images/whatsapp-icon.png"
        alt="WhatsApp"
        class="w-12 h-12 ml-2 cursor-pointer"
      />
      <button
        v-else
        @click="togglePopup"
        class="ml-2 w-12 h-12 flex items-center justify-center bg-green-500 rounded-full text-white cursor-pointer"
      >
        &#10005;
      </button>
    </div>

    <!-- Popup -->
    <div
      v-if="showPopup"
      class="fixed bottom-16 mb-4 right-4 rounded-xl bg-white shadow-lg w-72"
    >
      <div class="flex items-center bg-green-500 rounded-t-xl text-white w-full h-fit">
        <span class="mx-4 my-4 w-80 text-center"
          >Dapatkan informasi lengkap seputar promo dan pesanan Anda disini.</span
        >
      </div>
      <a
        class="flex items-center p-2 bg-gray-100 rounded-lg mt-2 mb-2 mx-2"
        href="https://wa.me/+6282264206100?text=Halo,%20saya%20tertarik%20mengetahui%20lebih%20lanjut%20layanan%20One%20Click%20Laundry.%20Bisa%20saya%20dapatkan%20informasi%20lebih%20lanjut?"
      >
        <button class="mx-2 text-green-500">
          <img src="@/assets/images/whatsapp-icon.png" alt="WhatsApp" class="w-12 h-12" />
        </button>
        <div>
          <div class="text-left font-bold">CS One Click Laundry</div>
        </div>
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "ChatButton",
  setup() {
    const showPopup = ref(false);

    const togglePopup = () => {
      showPopup.value = !showPopup.value;
    };

    return {
      showPopup,
      togglePopup,
    };
  },
});
</script>

<style scoped></style>
