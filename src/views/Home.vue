<template>
  <div class="home">
    <h1>Home</h1>
     
     <input type="text" v-model="search">

     <p>I risultati della ricerca per {{ search }}</p>
     <div v-for="name in filteredNames" :key="name">
      <h5>{{ name }}</h5>

     </div>
 



  </div>
</template>

<script>
import { ref, computed } from 'vue';


export default {
  name: 'Home',
  setup() {
   const search = ref('');
   const names = ref(['Gianluca', 'Matteo', 'Luigi', 'Francesco' , 'Daniele']);


   const filteredNames = computed(() => {
       return names.value.filter((name) => name.includes(search.value));
   });
   

     

     return {
       names,
       search,
       filteredNames
       
     }
  },
}
</script>
