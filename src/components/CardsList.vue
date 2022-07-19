<template>
  <div class="card">
      <div class="card-content">
         <div class="card-img">
            <img src="https://cloud.rtl.it/RTLFM/News/Article/600x600/buon-compleanno-freddie-mercury-avrebbe-75-anni-quel-giorno-al-live-aid-in-cui-fu-incoronato-re-square-site-tv25s.jpg" alt="freddie">
         </div>
         <div class="card-caption">
            <h3>Title</h3>
            <p>Subtitle</p>
         </div>
      </div>
   </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
   .card {
      width: calc(100% / 5);
      padding: 0.5rem 1rem;

      .card-content {
         background-color: rgba(255,255,255,.05);
         padding: 1rem;
         color: #fff
      }

      img {
         width: 100%;
      }

      .card-caption {
         padding: .5rem 0;

         h3 {
            text-transform: uppercase;
         }

         p {
            color: rgba(255,255,255,.5);
         }
      }
   }
</style>