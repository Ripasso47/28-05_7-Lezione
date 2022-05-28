<template>
  <div id="app">
    <Carousel @clicked="cliccato"/>
    <Domande :domanda="falla"/>
  </div>
</template>

<script>
import Carousel from './components/Macro/Carousel.vue'
import Domande from './components/Macro/Domande.vue'

export default {
  name: 'App',
  data(){
    return{
      falla: ''
    }
  },
  components: {
    Carousel,
    Domande,
  },
  methods: {
    cliccato(value){
      this.falla = value;
    },
  }
}
</script>

<style lang="scss">
#app {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  position: relative;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
