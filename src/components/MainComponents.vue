<template>
<div class="container text-center" id="main">
  <div class="row" style="padding-top: 30%;">
    <div class="col">
        <h1 class="halo">Halo, Aku Lovrisca</h1>
    </div>
  </div>
  <div class="row">
    <div class="col">
        <p class="deskripsi">Merupakan seorang mahasiswi Teknologi Informasi, Universitas Brawijaya</p>
    </div>
  </div>
  <div class="row" style="padding-top: 5%;">
    <div class="col">
        <div class="portofolio-box">
          <a href="#" class="portofolio" style="color: #0272F4;" @click.prevent="scrollToPortofolio">Portofolio</a>
        </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
    name: 'MainComponents',
    mounted() {
    this.scrollToPortofolio();
  },
  methods: {
    scrollToPortofolio() {
      const portofolio = document.getElementById('portofolio');
      portofolio.scrollIntoView({ behavior: 'smooth' });
    },
  },
}
</script>

<style>
div {
    font-family: 'PT Sans', 'Roboto', sans-serif;
}
.halo {
    font-style: normal;
    font-weight: bold;
    font-size: 50px;
    line-height: 65px;

    text-align: center;
    color: #000000;
}
.deskripsi {
    font-style: normal;
    font-weight: lighter;
    font-size: 18px;
    line-height: 26px;
    text-align: center;
    
    color: #000000;
}
.portofolio-box {
  display: inline-block;
  padding-top:10px;
  padding-bottom: 10px;
  padding-left: 50px;
  padding-right: 50px;
  border: 3px solid #0272F4;
  border-radius: 12px;
}
.portofolio {
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    line-height: 26px;
    text-decoration: none;
    
    text-align: center;
    color: #0272F4;
}
</style>