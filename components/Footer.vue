<!-- <template>
  <div class="footer">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 100"><path fill="#004080" fill-opacity="1" d="M0,128L1440,0L1440,320L0,320Z"></path></svg>
    <div class="footer-text">
      <p>Copyright <i class="fa-regular fa-copyright"></i> SMKN 4 Tasikmalaya 2024 - {{ year }}</p>
      <div>Made with ❤️ by Zulpa</div>
    </div>
  </div>
</template>

<script setup>
let year = new Date().getFullYear()
</script>

<style scoped>
.footer-text {
  background-color: #004080;
}
.footer {
  color: white;
  text-align: center;
  padding: 0.5rem 0;
  position: relative;
  width: 100%;
  font-size: 0.9rem;
  margin-top: 20px;
}
</style> -->

<template>
  <div class="bb">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#004080" fill-opacity="1" d="M0,160L48,170.7C96,181,192,203,288,197.3C384,192,480,160,576,165.3C672,171,768,213,864,202.7C960,192,1056,128,1152,101.3C1248,75,1344,85,1392,90.7L1440,96L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>
</div>
  <footer class="footer">
    <!-- Wave SVG -->
  
    <!-- Footer Content -->
    <div class="footer-content">
      <h2>SMKN 4 Tasikmalaya</h2>
      <p>
        Jl. Depok, Sukamenak, Kec. Purbaratu, Kab. Tasikmalaya, Jawa Barat 46196, Indonesia <br />
        &copy; 2024 - {{ year }} SMKN 4 Tasikmalaya. All rights reserved.
      </p>

      <!-- Social Media Links -->
      <div class="social-links">
        <a href="https://www.facebook.com/4smkn?mibextid=ZbWKwL" target="_blank">
          <i class="fab fa-facebook"></i>
        </a>
        <a href="https://www.instagram.com/smkn4tsmofficial?igsh=MTc3aTdrYjNpZzVodQ==" target="_blank">
          <i class="fab fa-instagram"></i>
        </a>
        <a href="https://www.tiktok.com/@smkn4tasikmalaya?_t=ZS-8skJP67Ot20&_r=1" target="_blank">
          <i class="fab fa-tiktok"></i>
        </a>
      </div>
    </div>
  </footer>
</template>

<script setup>
let year = new Date().getFullYear()
</script>

<style scoped>
/* Footer Styling */

.bb {
  margin-top: 555px;
}

.footer {
  position: relative;
  background-color: #004080;
  color: white;
  text-align: center;
  padding: 2rem 1rem;
  overflow: hidden;
  /* margin-top: 70px; */
}

.footer-content {
  z-index: 2;
  position: relative;
}

.footer h2 {
  margin-bottom: 0.5rem;
  font-size: 1.5rem;
}

.footer p {
  margin-bottom: 1.5rem;
  font-size: 0.9rem;
  line-height: 1.5;
}

/* Social Media Links */
.social-links {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.social-links a {
  color: white;
  font-size: 1.5rem;
  transition: transform 0.3s ease, color 0.3s ease;
}

.social-links a:hover {
  transform: scale(1.2);
  color: #7057f1;
}

/* Wave Animation */
.footer svg path {
  animation: wave 3s infinite ease-in-out;
}

@keyframes wave {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(15px);
  }
  100% {
    transform: translateX(0);
  }
}
</style>
