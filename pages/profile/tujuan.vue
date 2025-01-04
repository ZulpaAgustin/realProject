<script setup>
const desk = ref([
  {
    id: 1,
    des: 'Sekolah meraih prestasi pencapaian nilai rata-rata UN dan indeks integritas diatas rata-rata Nasional pada tahun 2026.'
  },
  {
    id:2,
    des: 'Sekolah Menghasilkan Tamatan yang siap bekerja Minimal 50 % Tamatan bekerja pada tahun tamat.'
  },
  {
    id:3,
    des: 'Terciptanya aktivitas dan kreatifitas yang positif oleh seluruh warga sekolah.'
  },
  {
    id:4,
    des: 'Sekolah meraih prestasi akademik dan non akademik minimal di tingkat provinsi Jawa Barat dan Nasional.'
  },
  {
    id:5,
    des: 'Sekolah memiliki tenaga pendidik dan kependidikan yang berkualifikasi minimal S1 dan linier dengan tugasnya, bersertifikat pendidik dan telah mengikuti diklat implementasi kurikulum merdeka pada tahun 2024.'
  }
]);

const tj = ref([...desk.value.slice(0,2)]);

const mulai = ref(tj.value.length);
const selesai = ref(mulai.value + 2);

const loading = () => {
  if (mulai.value < desk.value.length) {
    tj.value = [...tj.value, ...desk.value.slice(mulai.value, selesai.value)];
    mulai.value = selesai.value;
    selesai.value += 2;
  }
};
</script>

<template>
  <div>
    <div class="judul">
      <h2>Tujuan SMK Negeri 4 Tasikmalaya</h2>
    </div>
    <ul>
      <li v-for="deskripsi in tj" :key="deskripsi.id">
        {{ deskripsi.des }}
      </li>
      
    </ul>
    <button @click="loading" :disabled="tj.length === desk.length">Lanjut</button>
  </div>
  
</template>

<style scoped>
.judul {
  color: #004080;
  margin-top: 90px;
  text-align: center;
}

button{
  color: aliceblue;
  background-color: #004080;
}
</style>

<!-- <div class="card w-75">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Button</a>
  </div>
</div> -->

<!-- <li>Sekolah meraih prestasi pencapaian nilai rata-rata UN dan indeks integritas diatas rata-rata Nasional pada tahun 2026.</li>
      <li>Sekolah Menghasilkan Tamatan yang siap bekerja Minimal 50 % Tamatan bekerja pada tahun tamat.</li>
      <li>Terciptanya aktivitas dan kreatifitas yang positif oleh seluruh warga sekolah.</li>
      <li>Sekolah meraih prestasi akademik dan non akademik minimal di tingkat provinsi Jawa Barat dan Nasional.</li>
      <li>Sekolah memiliki tenaga pendidik dan kependidikan yang berkualifikasi minimal S1 dan linier dengan tugasnya, bersertifikat pendidik dan telah mengikuti diklat implementasi kurikulum merdeka pada tahun 2024.</li>
      <li>Sekolah mencapai kriteria sekolah berwawasan lingkungan (adiwiyata) pada tahun 2026.</li>
      <li>Sekolah terakreditasi dengan Nilai A pada tahun 2024.</li>
      <li>Sekolah memiliki Lembaga Sertifikasi Profesi (LSP) yang terlisensi, Tempat Uji Kompetensi (TUK) yang terverifikasi dan Bursa Kerja Khusus (BKK) yang terakreditasi pada tahun 2025.</li>
      <li>Sekolah memiliki Perpustakaan yang terakreditasi A pada tahun 2026.</li>
      <li>Sekolah menjadi Badan Layanan Umum Daerah (BLUD) pada tahun 2025.</li>
      <li>Sekolah mengimplementasikan Kurikulum Merdeka untuk seluruh tingkat pada tahun 2024.</li>
      <li>Sekolah memiliki Dokumen Kurikulum Merdeka untuk seluruh tingkat pada tahun 2024.</li>
      <li>Sekolah menerapkan Kurikulum Merdeka dengan Pembelajaran Berdiferensiasi dan Pembelajaran Sosial-Emosional untuk seluruh tingkat pada tahun 2024.</li>
      <li>Sekolah memiliki sarana prasaranasesuai dengan standar pelayanan minimal pendidikan dan standar IDUKA pada tahun 2026.</li>
      <li>Sekolah memiliki Teaching Factory di semua program keahlian yang sesuai dengan standar industri dan representatif pada tahun 2024.</li>
      <li>Sekolah melaksanakan program menumbuh kembangkan Budi Pekerti dan akhlak mulia melalui pendidikan karakter pada kegiatan, intra, ekstra kurikuler dan non kurikuler.</li> -->