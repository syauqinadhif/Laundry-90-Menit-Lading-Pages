<template>
  <div class="fixed z-50 py-4 px-16 w-full">
    <div
      class="py-4 px-12 item-center rounded-full transition-colors duration-200"
      :class="{ 'backdrop-blur-sm bg-white/75': scrollY > 10 }"
    >
      <div class="relative flex items-center justify-between">
        <a href="/" class="relative z-10">
          <img alt="Logo Laundry 90 Menit" :src="logo" class="w-28 select-none" />
        </a>
        <div class="absolute w-full">
          <nav class="w-fit px-6 mx-auto">
            <ul role="list" class="w-fit flex gap-x-8">
              <li>
                <a :href="'/'" :class="getNavClass('/')">Home</a>
              </li>
              <li>
                <a :href="'/layananKami'" :class="getNavClass('/layananKami')"
                  >Layanan Kami</a
                >
              </li>
              <li>
                <a :href="'/prices'" :class="getNavClass('/prices')">Daftar Harga</a>
              </li>
              <li>
                <a :href="'/promo'" :class="getNavClass('/promo')">Promo</a>
              </li>
              <li>
                <a :href="'/outlet'" :class="getNavClass('/outlet')">Outlet</a>
              </li>
            </ul>
          </nav>
        </div>
        <a
          href="/"
          class="relative flex z-10 px-8 py-2 bg-orange-500 font-medium text-white text-sm rounded-3xl"
        >
          Hubungi Kami
        </a>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import { useRoute } from "vue-router";
import logo from "@/assets/images/logo.png";

export default defineComponent({
  props: {
    scrollY: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {
      logo,
    };
  },
  setup() {
    const route = useRoute();
    const getNavClass = (path: string) => {
      return route.path === path
        ? "font-medium text-orange-500"
        : "font-medium text-darkgunmetal";
    };

    return {
      getNavClass,
    };
  },
});
</script>
