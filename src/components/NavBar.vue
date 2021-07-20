<template>
  <header>
      <h1>Blog</h1>
      <nav>
          <router-link :to="{ name: 'Home'}">
             <button>Home</button>
          </router-link>
          <router-link :to="{ name: 'Create'}">
            <button>Create Post</button>
          </router-link>
      </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style lang="scss">

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
     h1 {
         font-size: 40px;
         color: #dfdfdf;
     }
}

nav {
    display: flex;
     button {
         padding: 20px;
         margin: 0 11px;
         text-decoration: none;
     }
     a {
         text-decoration: none;
     }
  
}

</style>