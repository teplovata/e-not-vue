<template>
  <section class="py-16 bg-blue-50">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
        Никаких процентов с продаж. <br /> Только фиксированная плата.
      </h2>
      <div class="max-w-md mx-auto mt-10 bg-white rounded-2xl shadow-xl p-8 border border-blue-100">
        <h3 class="text-2xl font-semibold text-gray-800">Старт (Полный доступ)</h3>
        <div class="text-4xl font-bold text-blue-600 my-4">5 000 ₽<span class="text-lg text-gray-500">/мес</span></div>
        <ul class="text-left space-y-3 mt-6">
          <li v-for="(feature, index) in features" :key="index" class="flex items-start gap-2">
            <CheckCircleOutlined class="text-green-500 mt-1" />
            <span>{{ feature }}</span>
          </li>
        </ul>
        <div class="mt-8 bg-yellow-100 text-yellow-800 p-3 rounded-lg text-sm font-medium">
          🎁 Первым 10 клиентам — настройка в подарок и месяц бесплатно!
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { CheckCircleOutlined } from '@ant-design/icons-vue'

const features = [
  'Магазин в Telegram, VK, Max.',
  'Неограниченное кол-во товаров.',
  'Прием платежей.',
  'Простая админка.',
  'Поддержка при подключении.',
]
</script>