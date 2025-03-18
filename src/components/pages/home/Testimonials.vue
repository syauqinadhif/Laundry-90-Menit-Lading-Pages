<template>
  <div class="py-12 md:py-32 max-w-screen-xl mx-auto flex flex-col-reverse md:flex-row items-center">
    <!-- <div class="mt-8 w-3/4 md:w-1/2">
      <video
        controls
        class="w-11/12 md:w-1/2 md:h-1/2 rounded-xl shadow-xl mx-auto"
        data-aos="zoom-in"
        data-aos-duration="1000"
        src="@/assets/videos/profile-video.mp4"
        alt="Video tentang Laundry 90 Menit"
      ></video>
    </div> -->
    <div class="w-full pl-4 pr-4 md:mx-auto md:w-3/4 md:pl-8 text-center" data-aos="zoom-in" data-aos-duration="1000">
      <p class="text-primaryblue font-productsans font-semibold text-sm md:text-lg">
        Profile
      </p>
      <h2 class="font-vagrounded font-black text-2xl md:text-4xl text-richblack">
        One Click Laundry
      </h2>
      <p class="mt-2 md:mt-4 text-sm md:text-lg text-gunmetal font-productsans">
        One Click Laundry merupakan layanan laundry online di Yogyakarta yang memudahkan liburan Anda. Kami menyediakan
        layanan kiloan dan satuan dengan pilihan express 12 jam, 6 jam, dan 3 jam agar pakaian Anda bersih lebih cepat.
        Layanan antar-jemput kami mencakup seluruh wilayah Yogyakarta dengan biaya ongkir terjangkau. Cukup klik, kami
        jemput dan antar kembali pakaian anda dalam keadaan bersih.
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, onMounted } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";

export default defineComponent({
  name: "ProfileSection",
  setup() {
    onMounted(() => {
      AOS.init();
    });
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
</style>
