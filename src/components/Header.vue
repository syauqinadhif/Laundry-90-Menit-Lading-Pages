<template>
  <div class="fixed z-50 py-4 px-4 lg:px-16 w-full">
    <div
      class="py-4 px-4 lg:px-12 flex items-center justify-between rounded-full transition-colors duration-200"
      :class="{ 'backdrop-blur-sm bg-white/75': scrollY > 10 }"
    >
      <a href="/" class="relative z-10">
        <img alt="Logo Laundry 90 Menit" :src="logo" class="w-20 lg:w-28 select-none" />
      </a>
      <div class="hidden lg:flex relative items-center justify-between">
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
        class="hidden lg:block relative z-10 px-8 py-2 bg-orange-500 font-medium text-white text-sm rounded-3xl"
      >
        Hubungi Kami
      </a>
      <!-- Mobile Nav Button -->
      <div class="lg:hidden relative z-10">
        <button
          type="button"
          @click.stop="toggleMobileNav"
          :class="buttonClasses"
          class="w-fit mx-auto h-full p-4 flex items-center rounded-full transition-colors duration-200"
        >
          <GridOutline class="w-6 h-6 text-orange-500" />
        </button>
      </div>
      <!-- Mobile Nav Menu -->
      <nav
        v-if="openMobileNav"
        :class="navClasses"
        class="lg:hidden absolute right-0 mt-80 w-48 p-3 mx-auto rounded-lg text-center"
      >
        <ul role="list" class="w-full space-y-3">
          <li>
            <a
              @click.stop="closeMobileNav"
              href="/"
              class="block w-full font-medium text-sm text-darkgunmetal"
            >
              Home
            </a>
          </li>
          <li>
            <a
              @click.stop="closeMobileNav"
              href="/layananKami"
              class="block w-full font-medium text-sm text-darkgunmetal"
            >
              Layanan Kami
            </a>
          </li>
          <li>
            <a
              @click.stop="closeMobileNav"
              href="/prices"
              class="block w-full font-medium text-sm text-darkgunmetal"
            >
              Prices
            </a>
          </li>
          <li>
            <a
              @click.stop="closeMobileNav"
              href="/promo"
              class="block w-full font-medium text-sm text-darkgunmetal"
            >
              Promo
            </a>
          </li>
          <li>
            <a
              @click.stop="closeMobileNav"
              href="/outlet"
              class="block w-full font-medium text-sm text-darkgunmetal"
            >
              Outlets
            </a>
          </li>
          <li>
            <a
              @click.stop="closeMobileNav"
              href="https://lynk.id/bengkelinovasi"
              target="_blank"
              class="block w-full p-2 font-medium text-darkgunmetal bg-orange-500 text-white text-sm rounded-lg"
            >
              Hubungi Kami
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref, computed } from "vue";
import { useRoute } from "vue-router";
import logo from "@/assets/images/logo.png";
import GridOutline from "@/components/icons/GridOutline.vue"; // Adjust the path as necessary

export default defineComponent({
  components: {
    GridOutline,
  },
  props: {
    scrollY: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {
      logo,
      openMobileNav: false,
    };
  },
  setup() {
    const route = useRoute();
    const openMobileNav = ref(false);
    const scrollY = ref(window.scrollY);

    const getNavClass = (path: string) => {
      return route.path === path
        ? "font-medium text-orange-500"
        : "font-medium text-darkgunmetal";
    };

    const buttonClasses = computed(() => {
      return scrollY.value > 10 ? "backdrop-blur-sm bg-white/75" : "";
    });

    const navClasses = computed(() => {
      return scrollY.value > 10
        ? "backdrop-blur-sm bg-white/75 drop-shadow-md"
        : "bg-white";
    });

    const toggleMobileNav = () => {
      openMobileNav.value = !openMobileNav.value;
    };

    const closeMobileNav = () => {
      openMobileNav.value = false;
    };

    const onScroll = () => {
      scrollY.value = window.scrollY;
    };

    window.addEventListener("scroll", onScroll);

    return {
      getNavClass,
      openMobileNav,
      buttonClasses,
      navClasses,
      toggleMobileNav,
      closeMobileNav,
    };
  },
});
</script>

<style scoped>
/* Add any additional styles here */
</style>
