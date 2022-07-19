<template>
   <main>
      <div class="wrapper">
         <CardsList />
      </div>
   </main>
</template>

<script>
import CardsList from './CardsList.vue'

export default {
   components: {
      CardsList,
   }
}
</script>

<style lang="scss">
   main {
      height: calc(100% - 52px);
      padding: 4rem;

      .wrapper {
         display: flex;
         flex-wrap: wrap;
         width: 70%;
         margin: 0 auto;
      }
   }
</style>