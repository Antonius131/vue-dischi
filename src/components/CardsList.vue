<template>
   <div class="card-wrapper">
      <div class="card" v-for="(artist, index) in artistCard" :key="index">
         <div class="card-img">
            <img :src="artist.poster" :alt="artist.author">
         </div>
         <div class="card-caption">
            <h4>{{ artist.title }}</h4>
            <p>{{ artist.author }}</p>
            <p>{{ artist.year }}</p>
         </div>
      </div>
   </div>
</template>

<script>
import axios from 'axios';

export default {
   data: function() {
      return {
         artistCard: []
      }
   },
   methods: {
      getArtistCard() {
         axios.get('https://flynn.boolean.careers/exercises/api/array/music')
         .then((result) => {
            this.artistCard = result.data.response; 
            console.log(this.artistCard);
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

      .card {
      width: calc(100% / 5);
      height: 300px;
      background-color: rgba(255,255,255,.05);
      padding: 1rem;
      color: #fff;

         img {
            width: 100%;
         }

         .card-caption {
            padding: .5rem 0;

            h4 {
               text-transform: uppercase;
               margin-bottom: .75rem;
            }

            p {
               color: rgba(255,255,255,.3);
            }
         }
      }
   }

</style>