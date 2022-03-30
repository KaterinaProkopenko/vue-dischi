<template>
  <div id="app">
    <Header/>
    <Main/>
  </div>
</template>

<script>
import axios from "axios";
import Header from './components/Header.vue'
import Main from './components/Main.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  created: function(){
  this.getApiList()
  },

  methods: {
    getApiList(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
        console.log(result);
      })
      .catch((error) => {
        console.error(error);
      })
    }
  }

}

</script>

<style lang="scss">
@import './assets/style/main-style.scss';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
