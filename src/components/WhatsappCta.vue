<template>
  <div>
    <!-- Chat Button -->
    <div class="fixed bottom-4 right-4 flex items-center">
      <button
        @click="togglePopup"
        class="px-4 py-2 bg-white rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300"
      >
        <span>Butuh bantuan? Chat saja.</span>
      </button>
      <img
        @click="togglePopup"
        src="@/assets/images/whatsapp-icon.png"
        alt="WhatsApp"
        class="w-12 h-12 ml-2 cursor-pointer"
      />
    </div>

    <!-- Popup -->
    <div
      v-if="showPopup"
      class="fixed bottom-16 right-4 bg-white rounded-lg shadow-lg w-72 p-4"
    >
      <div class="flex items-center bg-green-500 text-white p-2 rounded-t-lg">
        <img
          src="@/assets/images/whatsapp-icon.png"
          alt="WhatsApp"
          class="w-6 h-6 mr-2"
        />
        <span>Ingin memulai percakapan?</span>
      </div>
      <div class="p-2 text-center border-b border-gray-200">
        Silakan tap logo <span class="font-bold">WhatsApp</span> dibawah ini
      </div>
      <div class="p-2 text-center text-gray-500">
        Pesan akan dibalas kurang dari 1 menit
      </div>
      <div class="flex items-center p-2 bg-gray-100 rounded-lg">
        <img src="@/assets/images/whatsapp-icon.png" alt="CS" class="w-12 h-12 mr-2" />
        <div>
          <div class="font-bold">CS Falisha Laundry</div>
          <div class="text-sm text-gray-500">Jagonya Laundry Ontime</div>
        </div>
        <button class="ml-auto text-green-500">
          <img src="@/assets/images/whatsapp-icon.png" alt="WhatsApp" class="w-6 h-6" />
        </button>
      </div>
      <button @click="togglePopup" class="absolute top-2 right-2 text-red-500">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M6 18L18 6M6 6l12 12"
          />
        </svg>
      </button>
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
