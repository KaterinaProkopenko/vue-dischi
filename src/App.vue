<template>
  <div id="app">
    <Header @select="updateSelectedGenre" :genres="genres"/>
    <Main @chosenGenres="updateGenresList" :selectedGenre="selectedGenreString"/>
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
      selectedGenreString: '',
      genres: []
    }
  },
  methods: {
    updateGenresList(genres){
      this.genres = genres;
    },

    updateSelectedGenre(selectedGenreString){
      this.selectedGenreString = selectedGenreString;
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
