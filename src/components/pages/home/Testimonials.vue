<template>
  <div
    class="py-12 md:py-32 max-w-screen-xl mx-auto flex flex-col md:flex-row-reverse items-center"
  >
    <div class="w-full pl-4 pr-4 md:mx-auto md:w-1/2 md:pl-8">
      <p class="text-orange-500 font-productsans font-semibold text-sm md:text-lg">
        Profile
      </p>
      <h2 class="font-vagrounded font-black text-2xl md:text-4xl text-richblack">
        Laundry 90 Menit
      </h2>
      <p class="mt-2 md:mt-4 text-sm md:text-lg text-gunmetal font-productsans">
        Selamat datang di Laundry 90 Menit! Nikmati pengalaman nge-laundry dengan mesin
        cuci modern yang lebih higienis dan praktis. Kami siap melayani Anda dengan
        layanan antar jemput khusus full service, serta menyediakan ruang tunggu yang
        nyaman bagi Anda yang memilih layanan self service. Datang dan buktikan kualitas
        layanan Laundry 90 Menit ya!
      </p>
    </div>
    <div class="mt-8 w-3/4 md:w-1/2 pr-8">
      <video
        controls
        class="w-full rounded-xl shadow-xl"
        data-aos="zoom-in"
        data-aos-duration="1000"
        src="@/assets/videos/laundry-90-mnt.mkv"
        alt="Video tentang Laundry 90 Menit"
      ></video>
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
