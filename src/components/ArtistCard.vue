<template>
   <div class="card">
      <div class="card-img">
         <img :src="poster" :alt="author">
      </div>
      <div class="card-caption">
         <h4>{{ title }}</h4>
         <p>{{ author }}</p>
         <p>{{ genre }}</p>
         <p>{{ year }}</p>
      </div>
   </div>
</template>

<script>
export default {
   props: {
      'title': String,
      'author': String,
      'poster': String,
      'year': String,
      'genre': String
   }
}
</script>

<style lang="scss">
   .card {
      width: calc(20% - 2rem);
      height: 310px;
      background-color: rgba(255,255,255,.05);
      margin: .75rem 1rem;
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
</style>