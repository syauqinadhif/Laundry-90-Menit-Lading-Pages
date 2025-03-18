<template>
  <div class="bg-cultured2 pt-8 md:pt-24 pb-14">
    <div class="max-w-screen-xl mx-auto">
      <h3
        class="w-5/6 md:w-full font-black px-6 text-2xl sm:text-5xl text-left md:text-center leading-tight"
      >
        <span class="text-gunmetal font-vagrounded">Mengapa</span>
        <span class="text-primaryblue font-vagrounded"> One Click Laundry</span
        ><span class="text-gunmetal font-vagrounded"> ?</span>
      </h3>
      <p
        class="font-productsans mt-2 sm:mt-6 px-6 sm:px-32 md:px-44 lg:px-64 text-left sm:text-center text-gunmetal text-sm sm:text-lg"
      >
        Lima Alasan Mengapa Anda Harus Memilih One Click Laundry Untuk Melayani Segala
        Kebutuhan Laundry Anda.
      </p>
      <div class="w-full mx-auto mt-8 md:mt-16 px-6 space-y-8">
        <div
          v-for="(reason, index) in reasons"
          :key="index"
          :class="
            index % 2 === 0
              ? 'flex flex-col sm:flex-row items-center justify-around max-w-full overflow-hidden '
              : 'flex flex-wrap items-center justify-around max-w-full overflow-hidden'
          "
        >
          <img
            :alt="'Gambar alasan ' + (index + 1)"
            :src="reason.img"
            :data-aos="index % 2 === 0 ? 'fade-right' : 'fade-left'"
            data-aos-duration="1000"
            class="pointer-events-none select-none h-80 w-100 rounded-2xl"
            :class="index % 2 === 0 ? '' : 'order-1 sm:order-2'"
          />
          <div
            :data-aos="index % 2 === 0 ? 'fade-left' : 'fade-right'"
            data-aos-duration="1000"
            :class="
              index % 2 === 0 ? 'mt-4 max-w-xl' : 'mt-4 max-w-xl order-2 sm:order-1'
            "
          >
            <p class="text-primaryblue text-xl sm:text-3xl">
              <span class="font-vagrounded font-black">#</span>
              <!-- <span class="font-vagrounded font-black">{{ index + 1 }}</span> -->
              <span class="font-vagrounded font-black">OneClick</span>
              <span class="font-vagrounded font-light">Laundry</span>
            </p>
            <p
              class="mt-0 md:mt-2.5 font-vagrounded font-black text-2xl sm:text-4xl text-gunmetal leading-tight"
            >
              {{ reason.title }}
            </p>
            <p class="mt-1.5 font-productsans sm:text-lg text-gunmetal">
              {{ reason.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import reason1Img from "@/assets/images/Mesin cuci canggih dan modern.jpg";
import reason2Img from "@/assets/images/Muat lebih  banyak.jpeg";
import reason3Img from "@/assets/images/Tidak mencampur pakaian.jpeg";
import reason4Img from "@/assets/images/No Drama.jpeg";
import reason5Img from "@/assets/images/Setrika anti gosong.jpg";

export default {
  name: "ReasonsSection",
  data() {
    return {
      reasons: [
        {
          img: reason1Img,
          title: "Menggunakan Mesin Cuci Modern dan Canggih",
          description:
            "Di One Click Laundry cucian kamu bakal jadi lebih bersih dan higienis",
        },
        {
          img: reason2Img,
          title: "Muat Lebih Banyak",
          description:
            "Mesin cuci dan pengering di One Click Laundry muat lebih banyak hingga 10 kg.",
        },
        {
          img: reason3Img,
          title: "Tidak Mencampur Pakaian",
          description:
            "Jaminan pakaian tidak dicampur untuk cuci kiloan dan satuan, cucian kamu dijamin tidak dicampur dengan cucian pelanggan lain.",
        },
        {
          img: reason4Img,
          title: "No Drama!",
          description:
            "Laundry no drama! Jaminan pakaian kamu tidak akan hilang atau tertukar: Sebelum pakaian kamu dicuci, crew outlet kami akan mencatat semua pakaian satu-persatu. Setelah prosesnya selesai, crew outlet akan melakukan konfirmasi ke kamu lewat whatsapp ya",
        },
        {
          img: reason5Img,
          title: "Jaminan Setrika Anti Gosong",
          description:
            "Seluruh outlet One Click Laundry sudah menggunakan setrika uap, jadi cucian kamu dijamin anti gosong dan berkerut",
        },
      ],
    };
  },
};
</script>
