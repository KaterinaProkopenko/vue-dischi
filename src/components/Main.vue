<template>
  <main>
      <div class="row justify-content-center m-0">
          <div class="col-8 d-flex justify-content-center flex-wrap py-5 gap">
                <MainCard v-for="(element, index) in cards" :key="index" :selectedGenre="selectedGenre" :cardObject="element"/>
          </div>
      </div>
  </main>
</template>

<script>
import axios from "axios";
import MainCard from './MainCard.vue';

export default {
    name: 'MainIndex',
    components: {
        MainCard,
    },
    props: ['selectedGenre'],

    data: function() {
        return {
            cards: null,
        }
    },

    created: function(){
        this.getApiList();
    },

    methods: {
        getApiList(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
                this.cards = result.data.response;
                console.log(this.cards);
            })
            .catch((error) => {
                console.error(error);
            })
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

main{
    width: 100%;
    background-color: $colorSecondary;

    div.gap{
        gap: 18px 30px;
    }
}

</style>