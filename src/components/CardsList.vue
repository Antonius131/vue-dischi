<template>
   <div class="card-wrapper">
      <ArtistCard />
   </div>
</template>

<script>
import ArtistCard from './ArtistCard.vue';
import axios from 'axios';

export default {
   components: { 
      ArtistCard,
   },
   data: function() {
      return {
         artistCard: []
      }
   },
   methods: {
      getArtistCard() {
         axios.get('https://flynn.boolean.careers/exercises/api/array/music')
         .then((result) => {
            console.log(result.data.response);
         });
      }
   },
   created() {
      this.getArtistCard();
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