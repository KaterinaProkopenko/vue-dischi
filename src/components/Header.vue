<template>
  <header class="ps-2 d-flex justify-content-between">
    <img src="https://brandlogos.net/wp-content/uploads/2021/12/spotify-brandlogo.net_.png" alt="logo">

    <div id="ms-select-input" class="input-group input-group-sm p-3">
      <select class="form-select" id="input-select" v-model="selectedString" @change="$emit('select', selectedString)">
        <option v-for="(genre, index) in genres" :value="genre" :key="index">{{genre}}</option>
      </select>
    </div>

  </header>
</template>

<script>

export default {
  name: 'HeaderIndex',
  props: ['genres'],
  data: function() {
      return {
        selectedString: '',
      }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/variables.scss';

  header{
    width: 100%;
    height: 60px;
    background-color: $colorPrimary;

    img{
      width: 45px;
      margin: .5rem;
    }

    div#ms-select-input{
      width: 300px;
      height: 20px;
    }
  }

</style>
