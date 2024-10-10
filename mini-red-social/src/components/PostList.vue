<!-- src/components/PostList.vue -->
<template>
    <div class="post-list space-y-4">
      <div v-for="post in posts" :key="post.id" class="post bg-white p-4 rounded-lg shadow">
        <h2 class="post-title text-xl font-bold text-blue-600">{{ post.title }}</h2>
        <p class="post-content text-gray-700">{{ post.content }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'PostList',
    props: {
      posts: {
        type: Array,
        required: true
      }
    }
  }
  </script>