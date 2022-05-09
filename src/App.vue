<template>
  <div id="app">
    <MenuComponent />
    <BannerComponent />
    <ServiceComponent />
    <CountComponent />
    <GreatWorkComponent/>
    <FooterComponent/>
  </div>
</template>

<script>
import MenuComponent from './components/Menu.vue'
import BannerComponent from './components/Banner.vue'
import ServiceComponent from './components/Service.vue'
import CountComponent from './components/Count.vue'
import GreatWorkComponent from './components/GreatWork.vue'
import FooterComponent from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    MenuComponent,
    BannerComponent,
    ServiceComponent,
    CountComponent,
    GreatWorkComponent,
    FooterComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
