<template>
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <div>
          <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            Один магазин — <span class="text-blue-600">работает везде.</span>
          </h2>
          <p class="text-lg text-gray-600">
            Подключили один раз в админке. Продаете в Telegram, Max и VK.
          </p>
        </div>
        <div class="bg-gray-100 p-6 rounded-2xl flex flex-col items-center justify-center">
          <div class="flex items-center space-x-4 md:space-x-8">
            <div class="bg-white p-3 rounded-full shadow-md"><TelegramOutlined class="text-3xl text-blue-500" /></div>
            <ArrowRightOutlined class="text-gray-400 text-xl" />
            <div class="bg-white p-3 rounded-full shadow-md"><i class="text-3xl text-blue-600">VK</i></div>
            <ArrowRightOutlined class="text-gray-400 text-xl" />
            <div class="bg-white p-3 rounded-full shadow-md"><MessageOutlined class="text-3xl text-blue-400" /></div>
          </div>
          <p class="text-sm text-gray-500 mt-4">Ваше облако e-not</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { TelegramOutlined, ArrowRightOutlined, MessageOutlined } from '@ant-design/icons-vue'
</script>