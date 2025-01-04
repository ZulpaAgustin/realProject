<script setup>
useHead({
  title: "Prestasi - Website Sekolah"
});

// Data prestasi
const prestasiList = [
  {
    title: "Duta Safety Riding",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/p1_7_11zon.webp",
    description: "Prestasi siswa siswi kami menjadi 'Duta Safety Riding' dan mendapatkan Beasiswa."
  },
  {
    title: "Juara 1 LKS Otomotif Tingkat Kota Tasikmalaya",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/p22_9_11zon.webp",
    description: "Sekolah kami berhasil meraih juara 1 lomba Motorcycle Repair & Maintenance."
  },
  {
    title: "Juara 3 02SN Atletik tingkat Jawa Barat",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/p33_10_11zon.webp",
    description: "Alhamdulillah siswa kami mendapatkan kejuaran dalam lomba Atletik."
  },
  {
    title: "Juara 2 Lomba Film Pendek dan Kriya",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/p11_8_11zon.webp",
    description: "Dalam ajang Film dan Kriya, siswa kami berhasil meraih juara 2."
  },
  {
    title: "Duta Safety Riding",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/p1_7_11zon.webp",
    description: "Prestasi siswa siswi kami menjadi 'Duta Safety Riding' dan mendapatkan Beasiswa."
  },
  {
    title: "Juara 1 LKS Otomotif Tingkat Kota Tasikmalaya",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/p22_9_11zon.webp",
    description: "Sekolah kami berhasil meraih juara 1 lomba Motorcycle Repair & Maintenance."
  },
  {
    title: "Juara 3 02SN Atletik tingkat Jawa Barat",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/p33_10_11zon.webp",
    description: "Alhamdulillah siswa kami mendapatkan kejuaran dalam lomba Atletik."
  },
  {
    title: "Juara 2 Lomba Film Pendek dan Kriya",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/p11_8_11zon.webp",
    description: "Dalam ajang Film dan Kriya, siswa kami berhasil meraih juara 2."
  },
];
</script>

<template>
  <div class="utama">
    <!-- Header -->
    <div class="container mt-5 text-center">
      <h1 class="mb-4">Prestasi Sekolah</h1>
      <p class="text-muted">Berikut adalah daftar prestasi yang telah diraih oleh siswa-siswi dan sekolah kami</p>
    </div>

    <!-- Daftar Prestasi -->
    <div class="container mt-4">
      <div class="row">
        <!-- Iterasi Prestasi -->
        <div
          v-for="(prestasi, index) in prestasiList"
          :key="index"
          class="col-md-6 mb-4"
        >
          <div class="card prestasi-card">
            <div class="image-wrapper">
              <img :src="prestasi.image" class="card-img-top" :alt="`Prestasi ${index + 1}`">
            </div>
            <div class="card-body">
              <h5 class="card-title">{{ prestasi.title }}</h5>
              <p class="card-text">{{ prestasi.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* CSS sama seperti sebelumnya */
.utama {
  margin-top: 90px;
}

h1 {
  color: #004080;
  text-transform: uppercase;
  letter-spacing: 2px;
  animation: fadeInUp 1s ease-out;
}

p {
  color: #555;
  font-size: 1.1rem;
  margin-bottom: 40px;
  animation: fadeInUp 1s ease-out 0.3s;
}

.image-wrapper {
  width: 100%;
  height: 200px;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.card-img-top {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card {
  border: none;
  border-radius: 10px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.card-body {
  background-color: #f9f9f9;
  padding: 20px;
}

.card-title {
  font-size: 1.25rem;
  font-weight: bold;
  color: #004080;
  transition: color 0.3s ease;
}

.card-text {
  color: #555;
  font-size: 1rem;
}

.card:hover .card-title {
  color: #003366;
}

.prestasi-card {
  opacity: 0;
  animation: fadeInUp 0.6s ease-out forwards;
}

.prestasi-card:nth-child(1) {
  animation-delay: 0.2s;
}

.prestasi-card:nth-child(2) {
  animation-delay: 0.4s;
}

.prestasi-card:nth-child(3) {
  animation-delay: 0.6s;
}

.prestasi-card:nth-child(4) {
  animation-delay: 0.8s;
}

/* Animations */
@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
