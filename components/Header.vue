<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<template>
  <div class="body">
    <nav class="navbar">
      <div class="logo">
        <img src="/assets/img/logopo.png" alt="Logo" />
        <h5>SMKN 4 Tasikmalaya</h5> 
      </div>
      <button class="menu-toggle" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </button>
      <ul class="nav-links" :class="{ active: isMenuOpen }"> 
        <li><nuxt-link to="/">Beranda</nuxt-link></li>
        <li><nuxt-link to="/profile/">Profile</nuxt-link></li>
        <li><nuxt-link to="/berita/">Berita</nuxt-link></li>
        <li><nuxt-link to="/prestasi/">Prestasi</nuxt-link></li>
        <li><nuxt-link to="/ekstra/">Ekstrakurikuler</nuxt-link></li>
        <li class="contact"><nuxt-link to="/kontak/">
          <button class="primary-btn">KONTAK KAMI</button></nuxt-link></li>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
button {
  border: none; 
  background: none; 
  outline: none; 
  transition: 0.5s; 
  cursor: pointer; 
}

.primary-btn {
  padding: 10px 20px; 
  font-size: 1rem; 
  line-height: 1; 
  background: #121a6a; 
  color: white; 
  border-radius: 5px; 
}

.contact {
  display: flex; 
  align-items: center; 
  height: 100%; 
}

.primary-btn:hover {
  background-color: #03031e; 
}

.navbar {
  position: fixed; 
  top: 0; 
  left: 0; 
  z-index: 1000; 
  display: flex; 
  justify-content: space-between; 
  align-items: center; 
  background-color: #004080; 
  color: white; 
  width: 100%; 
  height: 70px; 
  padding: 0; 
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); 
}

.nav-links a {
  color: white; 
  text-decoration: none; 
  font-size: 1rem;
  transition: color 0.3s ease; 
}

.logo {
  display: flex; 
  align-items: center; 
  gap: 1rem; 
  padding-left: 1rem; 
}
.logo img {
  height: 50px; 
  width: 50px; 
  object-fit: contain; 
}
.logo h5 {
  margin: 0; 
  font-size: 1.5rem; 
}

.nav-links {
  display: flex; 
  list-style: none; 
  gap: 1.5rem; 
  margin: 0; 
  padding-right: 1rem; 
}

.nav-links a:hover {
  color: #0077ff; 
}

.nav-links li {
  display: flex; 
  align-items: center; 
  height: 70px; 
}

.body {
  margin: 0; 
}

.menu-toggle {
  display: none;
  flex-direction: column;
  gap: 0.4rem;
  cursor: pointer;
}

.menu-toggle span {
  width: 25px;
  height: 3px;
  background: white;
  transition: 0.3s;
}

@media (max-width: 768px) {
  .menu-toggle {
    display: flex;
  }

  .nav-links {
    display: none;
    flex-direction: column;
    gap: 0;
    position: absolute;
    top: 70px;
    right: 0;
    background-color: #004080;
    width: 100%;
    padding: 1rem;
  }

  .nav-links.active {
    display: flex;
  }

  .nav-links li {
    text-align: center;
    height: auto;
  }
}
</style>
