<script setup>
import { ref } from "vue";

useHead({
  title: "Guru - Website Sekolah",
});

const supabase = useSupabaseClient();
const teachers = ref([]);
const start = ref(0);
const limit = 3;
const loading = ref(false);

const Loadmore = async () => {
  try {
    loading.value = true;
    const { data, error } = await supabase
      .from("guru")
      .select("id, nama, mapel, foto")
      .range(start.value, start.value + limit - 1);

    if (error) throw error;
    teachers.value = [...teachers.value, ...data];
    start.value += limit;
  } catch (err) {
    console.error("Error mengambil data:", err.message);
  } finally {
    loading.value = false;
  }
};

const totalData = ref(0);

const TotalTeachers = async () => {
  try {
    const { count, error } = await supabase
      .from("guru")
      .select("*", { count: "exact" });

    if (error) throw error;
    totalData.value = count;
  } catch (err) {
    console.error("Error mengambil total data:", err.message);
  }
};

Loadmore();
TotalTeachers();
</script>

<template>
  <div class="utama">
    <!-- Judul Halaman -->
    <div class="page-title">
      <h1 class="judul">Guru/Pendidik</h1>
      <p class="text-muted text-center">Guru-Guru SMKN 4 Tasikmalaya</p>
    </div>

    <!-- Kartu Guru -->
    <div class="row justify-content-center g-3">
      <div
        v-for="(teacher, index) in teachers"
        :key="index"
        class="col-md-4 d-flex justify-content-center align-items-stretch"
      >
        <div class="card teacher-card">
          <img :src="teacher.foto" alt="Foto Guru" class="card-img-top" />
          <div class="card-body text-center">
            <h5 class="card-title">{{ teacher.nama }}</h5>
            <p class="card-text">{{ teacher.mapel }}</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Tombol Load More -->
    <div class="text-center mt-4">
      <button
        class="btn btn-primary load-more-btn"
        @click="Loadmore"
        :disabled="loading"
        v-if="teachers.length < totalData || loading"
      >
        {{ loading ? "Memuat..." : "Muat Lebih Banyak" }}
      </button>
    </div>
  </div>
</template>

<style scoped>
/* Tata Letak Utama */
.utama {
  margin-top: 90px;
}

.page-title {
  text-align: center;
  margin-bottom: 2rem;
}

.judul {
  font-size: 2.5rem;
  font-weight: bold;
  color: #004080;
  margin-bottom: 0.5rem;
}

.page-title p {
  font-size: 1rem;
  color: #555;
}

/* Kartu Guru */
.teacher-card {
  width: 18rem;
  background-color: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.teacher-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
}

.teacher-card img {
  border-top-left-radius: 12px;
  border-top-right-radius: 12px;
  max-height: 220px;
  object-fit: cover;
}

.card-body {
  padding: 1rem;
}

.card-title {
  font-size: 1.2rem;
  font-weight: bold;
  color: #004080;
}

.card-text {
  font-size: 0.95rem;
  color: #666;
}

/* Tombol Load More */
.load-more-btn {
  padding: 0.8rem 2rem;
  font-size: 1rem;
  font-weight: bold;
  background: linear-gradient(to right, #004080, #002d66);
  color: #fff;
  border: none;
  border-radius: 8px;
  transition: background 0.3s ease, transform 0.3s ease;
}

.load-more-btn:hover {
  background: linear-gradient(to right, #002d66, #001b40);
  transform: translateY(-3px);
}

.load-more-btn:disabled {
  background: #ccc;
  cursor: not-allowed;
}
</style>
