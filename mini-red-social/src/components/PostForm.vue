<!-- src/components/PostForm.vue -->
<template>
    <form @submit.prevent="submitPost" class="post-form space-y-4 bg-white p-4 rounded-lg shadow">
      <input v-model="title" type="text" placeholder="Título" class="input-title w-full p-2 border rounded" required />
      <textarea v-model="content" placeholder="Contenido" class="input-content w-full p-2 border rounded" required></textarea>
      <button type="submit" class="submit-button bg-blue-500 text-white py-2 px-4 rounded hover:bg-blue-700">Publicar</button>
    </form>
  </template>
  
  <script>
  export default {
    name: 'PostForm',
    data() {
      return {
        title: '',
        content: ''
      }
    },
    methods: {
      submitPost() {
        this.$emit('submit-post', {
          id: Date.now(),
          title: this.title,
          content: this.content
        });
        this.title = '';
        this.content = '';
      }
    }
  }
  </script>