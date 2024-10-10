<!-- src/App.vue -->
<template>
  <div id="app" class="bg-gray-100 min-h-screen flex flex-col">
    <Navbar />
    <div class="flex-grow container mx-auto p-4">
      <PostForm @submit-post="addPost" />
      <PostList :posts="posts" />
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import PostForm from './components/PostForm.vue'
import PostList from './components/PostList.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Footer,
    PostForm,
    PostList
  },
  data() {
    return {
      posts: []
    }
  },
  methods: {
    addPost(post) {
      this.posts.push(post);
    }
  }
}
</script>