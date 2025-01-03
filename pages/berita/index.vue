<script setup>
useHead({
  title: "Berita Utama - Website Sekolah"
})
</script>

<template>
  <div class="utama news-page">
    <h1 class="page-title text-center mb-4">Berita Sekolah</h1>
    <div class="row">
      <!-- Card 1 -->
      <div class="col-md-4">
        <div class="card news-card">
          <img src="/assets/img/guru.jpg" class="card-img-top news-img" alt="Berita 1">
          <div class="card-body">
            <h5 class="card-title">Upacara Peringatan Hari Guru</h5>
            <p class="card-text">
              Upacara Peringatan Hari Guru Nasional Ke-30, dan HUT PGRI Ke-79 Tahun 2024.
              "Guru Hebat Indonesia Kuat".
            </p>
            <nuxt-link to="/berita/1/" class="btn btn-primary">Baca Selengkapnya</nuxt-link>
          </div>
        </div>
      </div>
      <!-- Card 2 -->
      <div class="col-md-4">
        <div class="card news-card">
          <img src="/assets/img/zona.jpg" class="card-img-top news-img" alt="Berita 2">
          <div class="card-body">
            <h5 class="card-title">Perencanaan Zona Integritas</h5>
            <p class="card-text">
              Zona Integritas di Satuan Pendidikan Dinas Pendidikan Provinsi Jawa Barat,
              Wujudkan Wilayah Bebas dari Korupsi & Birokrasi Bersih dan Melayani.
            </p>
            <nuxt-link to="/berita/2/" class="btn btn-primary">Baca Selengkapnya</nuxt-link>
          </div>
        </div>
      </div>
      <!-- Card 3 -->
      <div class="col-md-4">
        <div class="card news-card">
          <img src="/assets/img/septi.jpg" class="card-img-top news-img" alt="Berita 3">
          <div class="card-body">
            <h5 class="card-title">Skill Competition 2024</h5>
            <p class="card-text">
              Skill Competition 2024 di selenggarakan oleh Safety Riding Center PT Daya Adicipta Motora Bandung.
            </p>
            <nuxt-link to="/berita/3/" class="btn btn-primary">Baca Selengkapnya</nuxt-link>
          </div>
        </div>
      </div>
    </div>
    <!-- end -->
     
    <div class="row">
      <!-- Card 1 -->
      <div class="col-md-4">
        <div class="card news-card">
          <img src="/assets/img/guru.jpg" class="card-img-top news-img" alt="Berita 1">
          <div class="card-body">
            <h5 class="card-title">Upacara Peringatan Hari Guru</h5>
            <p class="card-text">
              Upacara Peringatan Hari Guru Nasional Ke-30, dan HUT PGRI Ke-79 Tahun 2024.
              "Guru Hebat Indonesia Kuat".
            </p>
            <nuxt-link to="/berita/1/" class="btn btn-primary">Baca Selengkapnya</nuxt-link>
          </div>
        </div>
      </div>
      <!-- Card 2 -->
      <div class="col-md-4">
        <div class="card news-card">
          <img src="/assets/img/zona.jpg" class="card-img-top news-img" alt="Berita 2">
          <div class="card-body">
            <h5 class="card-title">Perencanaan Zona Integritas</h5>
            <p class="card-text">
              Zona Integritas di Satuan Pendidikan Dinas Pendidikan Provinsi Jawa Barat,
              Wujudkan Wilayah Bebas dari Korupsi & Birokrasi Bersih dan Melayani.
            </p>
            <nuxt-link to="/berita/2/" class="btn btn-primary">Baca Selengkapnya</nuxt-link>
          </div>
        </div>
      </div>
      <!-- Card 3 -->
      <div class="col-md-4">
        <div class="card news-card">
          <img src="/assets/img/septi.jpg" class="card-img-top news-img" alt="Berita 3">
          <div class="card-body">
            <h5 class="card-title">Skill Competition 2024</h5>
            <p class="card-text">
              Skill Competition 2024 di selenggarakan oleh Safety Riding Center PT Daya Adicipta Motora Bandung.
            </p>
            <nuxt-link to="/berita/3/" class="btn btn-primary">Baca Selengkapnya</nuxt-link>
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
