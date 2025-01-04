<script setup>
useHead({
  title: "Hari Guru - Website Sekolah"
})
</script>

<template>
  <div class="utama">
    <div class="row">
      <!-- Konten Utama Berita -->
      <div class="col-lg-8">
        <div class="main-news">
          <img
            src="/assets/img/guru.jpg"
            alt="Berita Utama"
            class="main-news-image"
          />
          <p class="text-muted">Di Posting Tanggal 25 November 2024</p>
          <h2 class="main-news-title">Upacara Peringatan Hari Guru</h2>
          <p class="main-news-content">
            Upacara Peringatan Hari Guru Nasional Ke-30, dan HUT PGRI Ke-79 Tahun 2024. <br>
"Guru Hebat Indonesia Kuat"
          </p>
        </div>
      </div>

      <!-- Berita Lainnya -->
      <div class="col-lg-4">
        <div class="other-news">
          <h3 class="other-news-title">Berita Lainnya</h3>
          <div class="other-news-item">
            <img
              src="/assets/img/us.jpg"
              alt="Berita 1"
              class="other-news-image"
            />
            <div>
              <h5 class="other-news-heading">Ujian Sekolah(US)</h5>
              <nuxt-link to="/berita/beritaLain/us/" class="other-news-link">Baca Selengkapnya</nuxt-link>
            </div>
          </div>
          <div class="other-news-item">
            <img
              src="/assets/img/upcr.jpg"
              alt="Berita 2"
              class="other-news-image"
            />
            <div>
              <h5 class="other-news-heading">Upacara Sekolah</h5>
              <nuxt-link to="/berita/beritaLain/upacara/" class="other-news-link">Baca Selengkapnya</nuxt-link>
            </div>
          </div>
          <div class="other-news-item">
            <img
              src="/assets/img/uds.jpg"
              alt="Berita 3"
              class="other-news-image"
            />
            <div>
              <h5 class="other-news-heading">Job Fair</h5>
              <nuxt-link to="/berita/beritaLain/job/" class="other-news-link">Baca Selengkapnya</nuxt-link>
            </div>
          </div>
        </div> <br>
    
          <!-- Carousel -->
        <div class="other-news">
          <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img src="/assets/img/c.jpg" class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="/assets/img/z.jpg" class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="/assets/img/i.jpg" class="d-block w-100" alt="...">
              </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Next</span>
            </button>
          </div>
          <!-- end -->
        </div>
      </div>
      <!-- end -->
      
    </div>
  </div>
</template>

<style scoped>
.utama {
  margin-top: 90px;
}

.carousel {
  margin-top: 20px;
}

.carousel-inner img {
  border-radius: 8px;
}


/* Konten Utama Berita */
.main-news {
  padding: 20px;
}
.main-news-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
  margin-bottom: 15px;
}
.main-news-title {
  font-size: 2rem;
  color: #004080;
  margin-bottom: 10px;
}
.main-news-content {
  font-size: 1.1rem;
  color: #333;
  line-height: 1.6;
}

/* Berita Lainnya */
.other-news {
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
}
.other-news-title {
  font-size: 1.5rem;
  color: #004080;
  margin-bottom: 20px;
}
.other-news-item {
  display: flex;
  align-items: flex-start;
  margin-bottom: 15px;
}

.other-news-item > div {
  display: flex;
  flex-direction: column; /* Susun elemen secara vertikal */
}

.other-news-image {
  width: 80px;
  height: 80px;
  object-fit: cover;
  border-radius: 8px;
  margin-right: 10px;
}
.other-news-heading {
  font-size: 1rem;
  color: #333;
  /* margin: 0; */
  margin-bottom: 20px;
  margin: 0 0 5px 0;
}
.other-news-link {
  display: block;
  font-size: 0.9rem;
  color: #004080;
  text-decoration: none;
  margin-top: 5px;
}
.other-news-link:hover {
  text-decoration: underline;
}
</style>
