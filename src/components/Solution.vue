<template>
  <section class="py-16 bg-gradient-to-r from-indigo-50 to-blue-50">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
        Встречайте — мини-приложение e-not.
      </h2>
      <p class="text-lg text-gray-600 max-w-2xl mx-auto">
        Это не ссылка на сайт. Это полноценный магазин, который живет прямо в вашем канале или чате.
      </p>
      <div class="mt-8">
        <a-button 
          type="link"
          size="large"
          @click="$emit('showDemo')"
          class="text-blue-600 text-lg"
        >
          <template #icon><StarOutlined /></template>
          👉 Нажмите сюда, чтобы увидеть демо
        </a-button>
      </div>
      <div class="mt-8 max-w-md mx-auto bg-white p-4 rounded-2xl shadow-lg border">
        <p class="text-gray-500 mb-2">🖼️ Видео / гифка с работой магазина</p>
        <div class="bg-gray-200 h-32 rounded-lg flex items-center justify-center">
          <ShoppingCartOutlined class="text-4xl text-gray-400" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { StarOutlined, ShoppingCartOutlined } from '@ant-design/icons-vue'

defineEmits(['showDemo'])
</script>