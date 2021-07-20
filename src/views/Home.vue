<template>
  <div class="home">
    <h1>Home</h1>
     <div v-if="error">
        {{ error }}
      </div>
      <div v-if="posts.length">
        <PostList :posts="posts" />
      </div>

      <div v-else>
        <Spinner />
      </div>
     

     <button @click="showPosts = !showPosts">toggle posts</button>
 

    

  </div>
</template>

<script>

import PostList from '../components/PostList.vue';
import getPosts from '../composables/getPosts';
import Spinner from '../components/Spinner.vue';

export default {
  name: 'Home',
  components: { PostList , Spinner},
  setup() {
     
     const { posts, error, load} = getPosts();

     load();

     //const showPosts = ref(true);
    
     return {
      posts,
      error,
      //showPosts
       
     }
  },
}
</script>
