<template>
  <div id="app">
    <Header @change="chooseGenre" />
    <main>
      <Albums :infoGenre="option"/>
      
    </main>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Albums from './components/Albums.vue'

export default {
  name: 'App',
  components: {
    Header,
    Albums
  },
  data(){
    return{
      option:"",
    }
  },
  methods:{
    chooseGenre(txt){
      this.option=txt;
    }
  },
  
}
</script>

<style lang="scss">
@import "./assets/style/common";

</style>
