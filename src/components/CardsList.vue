<template>
   <div class="card-wrapper">
      <FilterSelect @filter="cardsFilter"/>
      <ArtistCard v-for="(artist, index) in artistsList" :key="index"
         :title = "artist.title"
         :author = "artist.author"
         :poster = "artist.poster"
         :genre = "artist.genre"
         :year = "artist.year"
      />
   </div>
</template>

<script>
import axios from 'axios';
import ArtistCard from './ArtistCard.vue';
import FilterSelect from './FilterSelect.vue';

export default {
   data: function () {
      return {
         artistsList: [],
         filteredArtists: []
      };
   },
   methods: {
      getArtistCard() {
         axios.get("https://flynn.boolean.careers/exercises/api/array/music")
               .then((result) => {
               this.artistsList = result.data.response;
         });
      },

      cardsFilter(needle) {
         console.warn(needle);
         const genreFilter = this.artistsList.filter((artist) => artist.genre.includes(needle));
         this.filteredArtists = genreFilter;
         console.log(this.filteredArtists);
      }
   },
   created() {
      this.getArtistCard();
   },
   components: {
    ArtistCard,
    FilterSelect
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