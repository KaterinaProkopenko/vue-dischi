<template>
  <div class="ms-card text-center ">
      <img class="img-fluid p-3" :src="cardObject.poster" :alt="cardObject.title">
      <h5 class="fw-bold mb-2 px-2 text-uppercase">{{cardObject.title}}</h5>
      <p class="m-0 lh-sm">{{cardObject.author}}</p>
      <p class="m-0 lh-sm">{{cardObject.year}}</p>
<!-- mx-3 mb-3 -->
  </div>
</template>

<script>
export default {
    name: 'MainCard',
    props: ['cardObject']

}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

    div.ms-card{
        width: 160px;
        height: 290px;
        background-color: $colorPrimary;

        h5{
            color: white;
        }

        p{
            color: $textColor;
            font-size: .9rem;
        }
    }

</style>