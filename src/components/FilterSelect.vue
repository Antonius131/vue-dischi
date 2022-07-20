<template>
   <div id="cards-filter">
      <select v-model="selectedValue">
         <option></option>
         <option>Rock</option>
         <option>Pop</option>
         <option>Jazz</option>
         <option>Metal</option>
      </select>
      <span>{{selectedValue}}</span>
   </div>
</template>

<script>
export default {
   data: function() {
      return {
         selectedValue: ''
      }
   }
}
</script>

<style lang="scss">
   #cards-filter {
      width: 100%;
      text-align: left;
      margin: 0rem 1rem 1rem 1rem;

      select {
         background: #fff;
         border: 1px solid #fff;
         padding: .25rem 1rem;
      }
   }
</style>