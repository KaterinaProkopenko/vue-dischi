<template>
  <header class="ps-2">
    <img src="https://brandlogos.net/wp-content/uploads/2021/12/spotify-brandlogo.net_.png" alt="logo">

  </header>
</template>

<script>
export default {
  name: 'HeaderIndex',
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
  }

</style>
