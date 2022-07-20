<template>
   <main>
      <CardsList />
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
      overflow: auto;
   }
</style>