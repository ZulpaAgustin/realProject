<script setup>
useHead({
  title: "Berita Utama - Website Sekolah",
});

// Data berita
const berita = [
  {
    id: 1,
    title: "Upacara Peringatan Hari Guru",
    description:
      "Upacara Peringatan Hari Guru Nasional Ke-30, dan HUT PGRI Ke-79 Tahun 2024. \"Guru Hebat Indonesia Kuat\".",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/guru.webp",
    link: "/berita/1/",
  },
  {
    id: 2,
    title: "Perencanaan Zona Integritas",
    description:
      "Zona Integritas di Satuan Pendidikan Dinas Pendidikan Provinsi Jawa Barat, Wujudkan Wilayah Bebas dari Korupsi & Birokrasi Bersih dan Melayani.",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/zona_4_11zon.webp",
    link: "/berita/2/",
  },
  {
    id: 3,
    title: "Skill Competition 2024",
    description:
      "Skill Competition 2024 di selenggarakan oleh Safety Riding Center PT Daya Adicipta Motora Bandung.",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/septi_19_11zon.webp",
    link: "/berita/3/",
  },
  {
    id: 4,
    title: "Upacara Peringatan Hari Guru",
    description:
      "Upacara Peringatan Hari Guru Nasional Ke-30, dan HUT PGRI Ke-79 Tahun 2024. \"Guru Hebat Indonesia Kuat\".",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/guru.webp",
    link: "/berita/1/",
  },
  {
    id: 5,
    title: "Perencanaan Zona Integritas",
    description:
      "Zona Integritas di Satuan Pendidikan Dinas Pendidikan Provinsi Jawa Barat, Wujudkan Wilayah Bebas dari Korupsi & Birokrasi Bersih dan Melayani.",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/zona_4_11zon.webp",
    link: "/berita/2/",
  },
  {
    id: 6,
    title: "Skill Competition 2024",
    description:
      "Skill Competition 2024 di selenggarakan oleh Safety Riding Center PT Daya Adicipta Motora Bandung.",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/septi_19_11zon.webp",
    link: "/berita/3/",
  },
  {
    id: 7,
    title: "Upacara Peringatan Hari Guru",
    description:
      "Upacara Peringatan Hari Guru Nasional Ke-30, dan HUT PGRI Ke-79 Tahun 2024. \"Guru Hebat Indonesia Kuat\".",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/guru.webp",
    link: "/berita/1/",
  },
  {
    id: 8,
    title: "Perencanaan Zona Integritas",
    description:
      "Zona Integritas di Satuan Pendidikan Dinas Pendidikan Provinsi Jawa Barat, Wujudkan Wilayah Bebas dari Korupsi & Birokrasi Bersih dan Melayani.",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/zona_4_11zon.webp",
    link: "/berita/2/",
  },
  {
    id: 9,
    title: "Skill Competition 2024",
    description:
      "Skill Competition 2024 di selenggarakan oleh Safety Riding Center PT Daya Adicipta Motora Bandung.",
    image: "https://wforcvieeatwxwymirhv.supabase.co/storage/v1/object/public/gambar/bebas/septi_19_11zon.webp",
    link: "/berita/3/",
  },
];
</script>

<template>
  <div class="utama news-page">
    <h1 class="page-title text-center mb-4">Berita Sekolah</h1>
    <div class="row">
      <!-- Perulangan Kartu -->
      <div class="col-md-4" v-for="item in berita" :key="item.id">
        <div class="card news-card">
          <img :src="item.image" class="card-img-top news-img" :alt="item.title">
          <div class="card-body">
            <h5 class="card-title">{{ item.title }}</h5>
            <p class="card-text">{{ item.description }}</p>
            <nuxt-link :to="item.link" class="btn btn-primary">Baca Selengkapnya</nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.utama {
  margin-top: 90px;
  margin-bottom: 20px;
  animation: fadeIn 1s ease-in-out;
}

.page-title {
  font-size: 2.5rem;
  color: #004080;
  text-transform: uppercase;
  letter-spacing: 2px;
  animation: slideIn 1s ease-out;
}

.news-img {
  height: 200px;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.news-img:hover {
  transform: scale(1.1);
}

.card {
  margin-bottom: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
}

.card-body {
  background-color: #f9f9f9;
}

.btn-primary {
  background-color: #004080;
  border-color: #003366;
  transition: background-color 0.3s ease;
}

.btn-primary:hover {
  background-color: #003366;
  border-color: #002244;
}

.news-card {
  opacity: 0;
  animation: fadeInUp 0.5s ease-in-out forwards;
}

.news-card:nth-child(1) {
  animation-delay: 0.3s;
}

.news-card:nth-child(2) {
  animation-delay: 0.6s;
}

.news-card:nth-child(3) {
  animation-delay: 0.9s;
}

/* Animation Definitions */
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes slideIn {
  0% {
    transform: translateY(-20px);
    opacity: 0;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
