
<script setup>
  import AddPeople from './components/AddPeople.vue'
</script>
<template>
  <v-app>
    <div class = "d-flex align-center flex-column mt-16" ><h1>Split your checks</h1>
      <h2>It's easy way to split your checks in 
      restaraunts and other places
    </h2>
  </div>
    <v-main>
      <div class = "d-flex align-center flex-column mt-7">
        <AddPeople></AddPeople>
    </div>
    </v-main>
    
  </v-app>
</template>



<style scoped>

</style>