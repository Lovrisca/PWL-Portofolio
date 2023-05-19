<template>
  <div class="home">
    <NavbarComponent></NavbarComponent>
    <MainComponents></MainComponents>
    <PortofolioComponent></PortofolioComponent>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarComponent from '@/components/NavbarComponent.vue'
import MainComponents from '@/components/MainComponents.vue'
import PortofolioComponent from '@/components/PortofolioComponents.vue'
import FooterComponent from '@/components/FooterComponent.vue'

export default {
  name: 'HomeView',
  components: {
    NavbarComponent,
    MainComponents,
    PortofolioComponent,
    FooterComponent
  }
}
</script>
