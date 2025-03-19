<template>
  <div class="w-full bg-blue-100 py-12">
    <div
      class="max-w-7xl mx-auto mb-12 px-4 flex flex-col lg:flex-row justify-between gap-x-16 items-start space-y-8 lg:space-y-0"
    >
      <!-- Logo and Description -->
      <div class="flex-1">
        <div class="flex items-center space-x-2">
          <!-- <img
            src="@/assets/images/illustration-hero.png"
            alt="QuickFold Logo"
            class="h-10 w-10"
          /> -->
          <span class="text-2xl font-vagrounded font-black text-gray-800"
            >One Click Laundry</span
          >
        </div>
        <p class="mt-4 text-gray-800">
          Laundry Express Antar-Jemput Seluruh Yogyakarta
        </p>
        <!-- <div class="mt-12">
          <span class="font-vagrounded font-black text-gray-800">Follow Us</span>
          <div class="flex space-x-4 mt-2">
            <a href="#" class="text-primaryblue">
              <i class="fab fa-facebook-f"></i>
            </a>
            <a href="#" class="text-blue-500">
              <i class="fab fa-x-twitter"></i>
            </a>
            <a href="#" class="text-primaryblue">
              <i class="fab fa-instagram"></i>
            </a>
          </div>
        </div> -->
      </div>

      <!-- Company Links -->
      <div class="flex-1">
        <h3 class="text-xl font-vagrounded font-black text-gray-800 mb-4">Company</h3>
        <ul class="space-y-2 text-gray-800">
          <li><a href="/" class="hover:underline">Home</a></li>
          <li><a href="/layananKami" class="hover:underline">Layanan Kami</a></li>
          <li><a href="/promo" class="hover:underline">Promo</a></li>
          <li><a href="/prices" class="hover:underline">Daftar Harga</a></li>
          <li><a href="/outlet" class="hover:underline">Outlet</a></li>
        </ul>
      </div>

      <!-- Further Links -->
      <!-- <div class="flex-1">
        <h3 class="text-xl font-semibold text-gray-800 mb-4">Further Links</h3>
        <ul class="space-y-2 text-gray-600">
          <li><a href="#" class="hover:underline">Terms and Condition</a></li>
          <li><a href="#" class="hover:underline">News</a></li>
          <li><a href="#" class="hover:underline">Recruitments</a></li>
          <li><a href="#" class="hover:underline">Privacy Policy</a></li>
        </ul>
      </div> -->

      <!-- Contact Info -->
      <div class="flex-1">
        <h3 class="text-xl font-vagrounded font-black text-gray-800 mb-4">
          Contact Info
        </h3>
        <ul class="space-y-3 text-gray-800">
          <li class="flex items-center space-x-2">
            <i class="fas fa-phone-alt text-primaryblue"></i>
            <span>082325643594</span>
          </li>
          <li class="flex items-center space-x-2">
            <i class="fas fa-envelope text-primaryblue"></i>
            <span>one1.click.laundry@gmail.com</span>
          </li>
          <li class="flex space-x-2">
            <i class="mt-1 fas fa-map-marker-alt text-primaryblue ml-1"></i>
            <span>
              Jl. Gito Gati ruko No.1, Penen, Donoharjo, Kec. Ngaglik, Kabupaten Sleman,
              Daerah Istimewa Yogyakarta 55581
            </span>
          </li>
        </ul>
      </div>
    </div>
    <div class="mt-8 text-center text-gray-800">
      <p>Copyright © 2025 One Click Laundry. All rights reserved</p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style scoped>
/* Include Font Awesome icons */
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");
</style>
