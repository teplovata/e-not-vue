<template>
  <section class="py-16 bg-gray-50">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl md:text-4xl font-bold text-center text-gray-900 mb-4">
        Подключение за 15 минут
      </h2>
      <div class="max-w-2xl mx-auto mt-10">
        <div v-for="(step, index) in steps" :key="index" class="flex items-start space-x-4 mb-4">
          <div class="bg-blue-500 text-white rounded-full w-8 h-8 flex items-center justify-center flex-shrink-0 font-bold">
            {{ index + 1 }}
          </div>
          <p class="text-gray-700 text-lg">{{ step }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  'Оставляете заявку.',
  'Я подключаю ваш магазин на своей стороне.',
  'Загружаете товары в простой админке.',
  'Получаете ссылку на мини-приложение.',
  'Продаете!',
]
</script>