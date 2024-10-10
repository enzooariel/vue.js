<!-- src/components/Navbar.vue -->
<template>
    <nav class="bg-blue-600 p-4 text-white">
      <div class="container mx-auto flex justify-between items-center">
        <div class="flex items-center space-x-4">
          <img src="../assets/img/wifi.png" alt="Logo" class="h-8 w-8" />
          <h1 class="text-2xl font-bold">Mini Red Social</h1>
        </div>
        <div class="space-x-4">
          <button class="bg-blue-700 hover:bg-blue-800 text-white py-2 px-4 rounded">Inicio</button>
          <button class="bg-blue-700 hover:bg-blue-800 text-white py-2 px-4 rounded">Perfil</button>
          <button class="bg-blue-700 hover:bg-blue-800 text-white py-2 px-4 rounded">Configuración</button>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navbar'
  }
  </script>