<template>
<div class="container text-center" id="portofolio">
  <div class="row" style="padding-top: 10%;">
    <div class="col">
      <p class="judul">PORTOFOLIO</p>
    </div>
  </div>

  <div class="row" style="padding-top: 1%;">
    <div class="col">
      <button @click="showWebsite" id="klik">Website</button>
    </div>
    <div class="col">
        <button @click="showMobile" id="klik">Aplikasi Mobile</button>
    </div>
    <div class="col">
        <button @click="showBasis" id="klik">Basis Data</button>
    </div>
    <div class="col">
        <button @click="showDesain" id="klik">Desain</button>
    </div>
  </div>

  <div class="row" style="padding-top: 5%;">

    <div v-if="!showDesainComponent && !showWebsiteComponent && !showMobileComponent && !showBasisComponent" class="col d-flex align-items-center justify-content-center">
      <div class="card" style="width: 18rem;">
        <img src="../assets/image/image1.png" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title">Puspa Florist</h5>
          <p class="card-text">Website antarmuka menggunakan html dan css</p>
          <a href="https://github.com/Lovrisca/Puspa-Florist" class="btn btn-primary" style="color: white;">Lihat Project</a>
        </div>
      </div>
    </div>

    <div v-if="!showDesainComponent && !showWebsiteComponent && !showMobileComponent && !showBasisComponent" class="col d-flex align-items-center justify-content-center">
      <div class="card" style="width: 18rem;">
        <img src="../assets/image/image2.png" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title">Gvyc Cafe</h5>
          <p class="card-text">Website antarmuka yang menerapkan prisip CRUD menggunakan php</p>
          <a href="https://github.com/Lovrisca/Project-Akhir-PAW" class="btn btn-primary" style="color: white;">Lihat Project</a>
        </div>
      </div>
    </div>

    <div v-if="showWebsiteComponent">
        <WebsiteComponent />
    </div>

    <div v-if="showDesainComponent">
        <DesainComponent />
    </div>

    <div v-if="showMobileComponent">
        <MobileComponent/>
    </div>

    <div v-if="showBasisComponent">
        <BasisComponent/>
    </div>

  </div>

</div>
</template>

<script>
import DesainComponent from "@/components/DesainComponent.vue"; 
import WebsiteComponent from "@/components/WebsiteComponent.vue";
import MobileComponent from "@/components/MobileComponents.vue";
import BasisComponent from "@/components/BasisComponent.vue";

export default {
  name: "PortofolioComponent",
  components: {
    DesainComponent,
    WebsiteComponent,
    MobileComponent,
    BasisComponent,
  },
  data() {
    return {
      showDesainComponent: false,
      showWebsiteComponent: false,
      showMobileComponent: false,
      showBasisComponent: false,
    };
  },
  methods: {
    showDesain() {
      this.showDesainComponent = true;
      this.showWebsiteComponent = false;
      this.showMobileComponent = false;
      this.showBasisComponent = false;
    },
    showWebsite() {
      this.showWebsiteComponent = true;
      this.showDesainComponent = false;
      this.showMobileComponent = false;
      this.showBasisComponent = false;
    },
    showMobile() {
      this.showMobileComponent = true;
      this.showWebsiteComponent = false;
      this.showDesainComponent = false;
      this.showBasisComponent = false;
    },
    showBasis() {
      this.showBasisComponent = true;
      this.showMobileComponent = false;
      this.showWebsiteComponent = false;
      this.showDesainComponent = false;
    }
  },
};
</script>

<style>
div {
    font-family: 'PT Sans', 'Roboto', sans-serif;
}
.judul {
    font-style: normal;
    font-weight: 700;
    font-size: 25px;
    line-height: 32px;
    text-align: center;
    color: #000000;
}
.col a{
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    line-height: 26px;
    text-align: center;
    color: #000000;
}

#klik {
  color: white;
  background: #0272F4;
  border-radius: 20px;
  padding-top: 12px;
  padding-bottom: 12px;
  padding-right: 25px;
  padding-left: 25px;
}
</style>