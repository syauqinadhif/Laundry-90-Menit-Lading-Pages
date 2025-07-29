<template>
  <div class="max-w-screen-xl mx-auto py-28 md:py-32 p-4">
    <h1 class="text-center text-2xl lg:text-4xl mb-2 font-vagrounded font-black text-gray-800">
      LAYANAN KAMI
    </h1>
    <div class="w-24 lg:w-48 h-1 bg-primaryblue mt-4 mb-6 lg:mb-12 mx-auto"></div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      
      <!-- Cuci Setrika -->
      <div class="bg-softgray rounded-2xl shadow-lg p-6 flex flex-col justify-between h-full">
        <div>
          <h2 class="text-xl font-vagrounded font-black text-primaryblue mb-4">Cuci Setrika/kg</h2>
          <ul class="mb-4">
            <li class="flex items-center mb-2">
              <img src="@/assets/images/cuci-setrika.svg" alt="Cuci Setrika" class="w-6 h-6 mr-2" />
              <span class="font-productsans flex-grow">1 Hari</span>
              <span class="font-productsans">Rp10.000</span>
            </li>
            <li class="flex items-center mb-2">
              <img src="@/assets/images/cuci-setrika.svg" alt="Cuci Setrika" class="w-6 h-6 mr-2" />
              <span class="font-productsans flex-grow">12 Jam</span>
              <span class="font-productsans">Rp14.000</span>
            </li>
            <li class="flex items-center mb-2">
              <img src="@/assets/images/cuci-setrika.svg" alt="Cuci Setrika" class="w-6 h-6 mr-2" />
              <span class="font-productsans flex-grow">6 Jam</span>
              <span class="font-productsans">Rp16.000</span>
            </li>
            <li class="flex items-center mb-2">
              <img src="@/assets/images/cuci-setrika.svg" alt="Cuci Setrika" class="w-6 h-6 mr-2" />
              <span class="font-productsans flex-grow">3 Jam</span>
              <span class="font-productsans">Rp20.000</span>
            </li>
          </ul>
        </div>
        <div class="mt-4 flex justify-end">
          <a 
            href="https://wa.me/6282264206100?text=Halo,%20saya%20tertarik%20dengan%20paket%20Laundry%20Cuci%20Setrika.%20Bisa%20saya%20dapatkan%20informasi%20lebih%20lanjut?"
            target="_blank"
            class="bg-primaryblue text-white font-productsans py-2 px-6 rounded-full hover:bg-orange-600 transition"
          >
            Order
          </a>
        </div>
      </div>

      <!-- Cuci Lipat -->
      <div class="bg-softgray rounded-2xl shadow-lg p-6 flex flex-col justify-between h-full">
        <div>
          <h2 class="text-xl font-vagrounded font-black text-primaryblue mb-4">Cuci Lipat/kg</h2>
          <ul class="mb-4">
            <li class="flex items-center mb-2">
              <img src="@/assets/images/cuci-lipat.svg" alt="Cuci Lipat" class="w-6 h-6 mr-2" />
              <span class="font-productsans flex-grow">6 Jam</span>
              <span class="font-productsans">Rp12.000</span>
            </li>
            <li class="flex items-center mb-2">
              <img src="@/assets/images/cuci-lipat.svg" alt="Cuci Lipat" class="w-6 h-6 mr-2" />
              <span class="font-productsans flex-grow">3 Jam</span>
              <span class="font-productsans">Rp17.000</span>
            </li>
          </ul>
        </div>
        <div class="mt-4 flex justify-end">
          <a 
            href="https://wa.me/6282264206100?text=Halo,%20saya%20tertarik%20dengan%20paket%20Laundry%20Cuci%20Lipat.%20Bisa%20saya%20dapatkan%20informasi%20lebih%20lanjut?"
            target="_blank"
            class="bg-primaryblue text-white font-productsans py-2 px-6 rounded-full hover:bg-orange-600 transition"
          >
            Order
          </a>
        </div>
      </div>

      <!-- Setrika Saja -->
      <div class="bg-softgray rounded-2xl shadow-lg p-6 flex flex-col justify-between h-full">
        <div>
          <h2 class="text-xl font-vagrounded font-black text-primaryblue mb-4">Setrika Saja/kg</h2>
          <ul class="mb-4">
            <li class="flex items-center mb-2">
              <img src="@/assets/images/setrika.svg" alt="Setrika Saja" class="w-6 h-6 mr-2" />
              <span class="font-productsans flex-grow">1 Hari</span>
              <span class="font-productsans">Rp6.500</span>
            </li>
            <li class="flex items-center mb-2">
              <img src="@/assets/images/setrika.svg" alt="Setrika Saja" class="w-6 h-6 mr-2" />
              <span class="font-productsans flex-grow">2 Hari</span>
              <span class="font-productsans">Rp4.500</span>
            </li>
          </ul>
        </div>
        <div class="mt-4 flex justify-end">
          <a 
            href="https://wa.me/6282264206100?text=Halo,%20saya%20tertarik%20dengan%20paket%20Laundry%20Setrika%20Saja.%20Bisa%20saya%20dapatkan%20informasi%20lebih%20lanjut?"
            target="_blank"
            class="bg-primaryblue text-white font-productsans py-2 px-6 rounded-full hover:bg-orange-600 transition"
          >
            Order
          </a>
        </div>
      </div>
      <!-- Harga Paket -->
<!-- Paket Berlangganan Mingguan -->
<div class="bg-softgray rounded-2xl shadow-lg p-6 flex flex-col justify-between h-full">
  <div>
    <h2 class="text-xl font-vagrounded font-black text-primaryblue mb-4">Paket Berlangganan</h2>
    <ul class="text-md text-gray-700 pl-4 list-disc mb-4">
      <li>Rp175.000 untuk 4x cuci</li>
      <li>Setiap cuci maksimal 5kg</li>
      <li>Gratis ongkir jarak 3km</li>
      <li>Berlaku selama 30 hari</li>
      <li>Durasi pengerjaan 1 hari</li>
    </ul>
  </div>
  <div class="mt-4 flex justify-end">
    <a 
      href="https://wa.me/6282264206100?text=Halo,%20saya%20tertarik%20dengan%20Paket%20Berlangganan%20Mingguan.%20Bisa%20saya%20dapatkan%20informasi%20lebih%20lanjut?"
      target="_blank"
      class="bg-primaryblue text-white font-productsans py-2 px-6 rounded-full hover:bg-orange-600 transition"
    >
      Order
    </a>
  </div>
</div>
<!-- Paket Mahasiswa -->
<div class="bg-softgray rounded-2xl shadow-lg p-6 flex flex-col justify-between h-full">
  <div>
    <h2 class="text-xl font-vagrounded font-black text-primaryblue mb-4">Paket Mahasiswa</h2>
    <ul class="text-md text-gray-700 pl-4 list-disc mb-4">
      <li>Tunjukkan KTM</li>
      <li>Rp8.000/kg (1 hari jadi)</li>
      <li>Diskon 20% untuk semua layanan express</li>
    </ul>
  </div>
  <div class="mt-4 flex justify-end">
    <a 
      href="https://wa.me/6282264206100?text=Halo,%20saya%20tertarik%20dengan%20Paket%20Mahasiswa.%20Bisa%20saya%20dapatkan%20informasi%20lebih%20lanjut?"
      target="_blank"
      class="bg-primaryblue text-white font-productsans py-2 px-6 rounded-full hover:bg-orange-600 transition"
    >
      Order
    </a>
  </div>
</div>



    </div>
  </div>
</template>
