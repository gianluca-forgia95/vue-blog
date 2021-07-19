<template>
  <div class="home">
    <h1>Home</h1>
     
     <PostList v-if="showPosts" :posts="posts" />

     <button @click="showPosts = !showPosts">toggle posts</button>
 

    

  </div>
</template>

<script>
import { ref } from 'vue';
import PostList from '../components/PostList.vue';


export default {
  components: { PostList },
  name: 'Home',
  components: { PostList },
  setup() {
     const posts = ref([]);

     const error = ref(null);

     const showPosts = ref(true);

     const load = async () => {
       try {

       }
       catch (err) {
         let data = await fetch('http/')
       }
     }

    
     return {
      posts,
      showPosts
       
     }
  },
}
</script>
