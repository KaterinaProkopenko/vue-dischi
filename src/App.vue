<template>
  <div id="app">
    <Header @select="selectedGenre"/>
    <Main :selectedGenre="selectedString"/>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Main from './components/Main.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data: function() {
    return {
      selectedString: '',
    }
  },
  methods: {
    selectedGenre(string){
      this.selectedString = string;
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
