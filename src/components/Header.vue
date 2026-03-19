<template>
  <header class="sticky top-0 z-50 bg-white/80 backdrop-blur-md shadow-sm">
    <div class="container mx-auto px-4 py-3 flex justify-between items-center">
      <div class="flex items-center space-x-2">
        <span class="text-2xl">🦝</span>
        <span class="font-bold text-xl text-gray-800">e-not</span>
      </div>
      
      <div class="flex items-center space-x-3">
        <a-button 
          type="text" 
          @click="$emit('showDemo')"
          class="hidden sm:inline-flex"
        >
          Посмотреть как работает
        </a-button>
        <a-button 
          type="primary"
          @click="$emit('openForm')"
          class="bg-blue-500 hover:bg-blue-600"
        >
          Оставить заявку
        </a-button>
      </div>
    </div>
  </header>
</template>

<script setup>
defineEmits(['showDemo', 'openForm'])
</script>