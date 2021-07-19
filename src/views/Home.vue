<template>
  <div class="home">
    <h1>Home</h1>

    <h2>Refs</h2>

    <p>{{ person.name }} - {{ person.age }}</p>


    <button @click="updatePerson">Modifica l'età</button>

    <h2>Reactive</h2>

    <p>{{ personTwo.name }} - {{ personTwo.age }}</p>

    <button @click="updatePersonTwo">Modifica l'età</button>



  </div>
</template>

<script>
import { ref, reactive } from 'vue';


export default {
  name: 'Home',
  setup() {
    //  const p = ref('hello');
    //  console.log(p.value);
     const person = ref({ name: 'Gianluca', age: 26 });
     const personTwo = reactive({ name: 'Mario', age: 30});

     const updatePerson = () => {
       person.value.age = 25;
    
     }
     const updatePersonTwo = () => {
       personTwo.age = 20;
    
     }

     return {
      person,
      updatePerson,
      personTwo,
      updatePersonTwo
     }
  },
}
</script>
