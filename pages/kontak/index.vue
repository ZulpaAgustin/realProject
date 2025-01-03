<script setup>
useHead({
  title: "Kontak - Website Sekolah"
})
</script>

<template>
  <div class="utama">
    <div class="contact-container">
      <!-- Bagian kiri: Formulir Kontak -->
      <div class="form-section">
        <h2>Kontak Kami</h2>
        <form>
          <div class="form-group">
            <label for="name">Nama</label>
            <input type="text" id="name" placeholder="Masukkan nama Anda" />
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" placeholder="Masukkan email Anda" />
          </div>
          <div class="form-group">
            <label for="message">Pesan</label>
            <textarea id="message" rows="5" placeholder="Tulis pesan Anda di sini"></textarea>
          </div>
          <button type="submit" class="primary-btn">Kirim Pesan</button>
        </form>
      </div>

      <!-- Bagian kanan: Gambar -->
      <div class="image-section">
        <img src="/assets/img/main.jpg" alt="Kontak Kami" />
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Struktur dasar */
.utama {
  margin-top: 90px;
}

.contact-container {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  background: linear-gradient(to right, #f8f9fa, #e6eaf0);
}

/* Bagian Formulir */
.form-section {
  flex: 1;
  max-width: 500px;
  padding: 1.5rem;
  background-color: #fff;
  border-radius: 12px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
  animation: fadeIn 1s ease-in-out;
}

.form-section h2 {
  margin-bottom: 1.5rem;
  color: #004080;
  font-size: 2rem;
  text-align: center;
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  font-weight: bold;
  margin-bottom: 0.5rem;
  color: #333;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.8rem;
  border: 1px solid #ddd;
  border-radius: 8px;
  font-size: 1rem;
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #004080;
  box-shadow: 0 0 8px rgba(0, 64, 128, 0.2);
}

.primary-btn {
  display: block;
  width: 100%;
  padding: 1rem;
  background: linear-gradient(to right, #004080, #002d66);
  color: #fff;
  border: none;
  border-radius: 8px;
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.3s ease, transform 0.3s ease;
}

.primary-btn:hover {
  background: linear-gradient(to right, #002d66, #001b40);
  transform: translateY(-3px);
}

/* Bagian Gambar */
.image-section {
  flex: 1;
  max-width: 500px;
  text-align: center;
  padding: 1.5rem;
  animation: slideIn 1s ease-in-out;
}

.image-section img {
  max-width: 100%;
  height: auto;
  border-radius: 12px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.image-section img:hover {
  transform: scale(1.05);
  box-shadow: 0 12px 25px rgba(0, 0, 0, 0.3);
}

/* Animasi menggunakan keyframes */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideIn {
  from {
    opacity: 0;
    transform: translateX(20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>
