<template>
  <div class="home">
    <h1>Home</h1>
    
     <div v-if="error">
        {{ error }}
      </div>
      <div v-if="posts.length">
        <PostList :posts="posts" />
        <TagCloud :posts="posts" />
      </div>

      <div v-else>
        <Spinner />
      </div>
 

    

  </div>
</template>

<script>

import PostList from '../components/PostList.vue';
import TagCloud from '../components/TagCloud.vue';
import getPosts from '../composables/getPosts';
import Spinner from '../components/Spinner.vue';

export default {
  name: 'Home',
  components: { PostList , Spinner, TagCloud},
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


<style>

.home {
  max-width: 1200px;
  margin: 0 auto;
  padding: 10px;
}


</style>
