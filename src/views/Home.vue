<template>
  <div class="home">
     <p>My name is {{ name }} and my age is {{ age }}</p>

     <button @click="handleClick">Click</button>
  </div>
</template>

<script>


export default {
  name: 'Home',
  setup() {
     console.log('setup');

     let name = 'Gianluca';
     let age = 30;

     const handleClick = () => {
       console.log('click');
     }

     return {
      name,
      age,
      handleClick,
     }
  },
}
</script>
