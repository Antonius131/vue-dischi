<template>
   <div class="card-wrapper">
      <ArtistCard />
   </div>
</template>

<script>
import axios from 'axios';
import ArtistCard from './ArtistCard.vue';

export default {
   data: function () {
      return {
         artistCard: []
      };
   },
   methods: {
      getArtistCard() {
         axios.get("https://flynn.boolean.careers/exercises/api/array/music")
               .then((result) => {
               this.artistCard = result.data.response;
               console.log(this.artistCard);
         });
      }
   },
   created() {
      this.getArtistCard();
   },
   components: { 
   ArtistCard 
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