<template>
  <div>
   <post-form @create="createPost"/>
   <post-list :posts="posts"/>
  </div>
</template>

<script>

import PostForm from './components/PostForm.vue';
import PostList from './components/PostList.vue';

export default {
  name: 'App',
  components: {
    PostForm, PostList
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'Js title', body: 'About JS'},
        {id: 2, title: 'React title', body: 'About React'},
        {id: 3, title: 'Vue title', body: 'About Vue'},
        {id: 4, title: 'Angular title', body: 'About Angular'},
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    }
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#app {
  padding: 20px;
}

</style>
