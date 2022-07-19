<template>
  <div class="card-wrapper">
      <ArtistCard />
   </div>
</template>

<script>
import ArtistCard from './ArtistCard.vue';

export default {
   components: { 
      ArtistCard,
   }
}
</script>

<style lang="scss">

   .card-wrapper {
      display: flex;
      flex-wrap: wrap;
      width: 70%;
      margin: 0 auto;
   }

</style>