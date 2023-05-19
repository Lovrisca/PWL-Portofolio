<template>
<nav class="navbar navbar-expand-lg bg-body-tertiary fixed-top" style="background-color: white;">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
        <img src="../assets/image/logo.png" width="50">
    </a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <a class="nav-link" href="#" @click.prevent="scrollToMain">BERANDA</a>
        <a class="nav-link" href="#" @click.prevent="scrollToPortofolio">PORTOFOLIO</a>
        <a class="nav-link" href="#" id="kontak" @click.prevent="scrollToFooter">KONTAK</a>
      </div>
    </div>
  </div>
</nav>
</template>

<script>
export default {
    name: 'NavbarComponent',
    mounted() {
    this.scrollToFooter();
    this.scrollToPortofolio();
    this.scrollToMain();
  },
  methods: {
    scrollToFooter() {
      const footer = document.getElementById('footer');
      footer.scrollIntoView({ behavior: 'smooth' });
    },
    scrollToPortofolio() {
      const portofolio = document.getElementById('portofolio');
      portofolio.scrollIntoView({ behavior: 'smooth' });
    },
    scrollToMain() {
      const main = document.getElementById('main');
      main.scrollIntoView({ behavior: 'smooth' });
    },
  },
}
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
}
.navbar-nav {
  margin-left: auto;
  color: black;
}
.nav-link {
    margin-right: 20px;
}
#kontak {
    color: white;
    background: #0272F4;
    border-radius: 12px;
}
a {
    font-family: 'PT Sans', 'Roboto', sans-serif;
}
</style>