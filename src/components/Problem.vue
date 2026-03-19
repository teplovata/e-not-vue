<template>
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl md:text-4xl font-bold text-center text-gray-900 mb-4">
        Надоело терять деньги на комиссиях и переходах?
      </h2>
      <div class="grid md:grid-cols-3 gap-6 mt-12">
        <div v-for="(item, index) in problems" :key="index" 
             class="bg-gray-50 p-6 rounded-xl border border-gray-100 hover:shadow-md transition">
          <component :is="item.icon" class="text-3xl mb-3" />
          <h3 class="text-xl font-semibold mb-2">{{ item.title }}</h3>
          <p class="text-gray-600">{{ item.desc }}</p>
        </div>
      </div>
      <p class="text-center text-lg font-medium text-gray-700 mt-8 bg-blue-50 p-4 rounded-xl">
        💡 Ваши клиенты уже здесь, в Telegram, MAX и VK. Нужно просто дать им удобную витрину.
      </p>
    </div>
  </section>
</template>

<script setup>
import { ShoppingCartOutlined, ArrowRightOutlined, SmileOutlined } from '@ant-design/icons-vue'

const problems = [
  { icon: ShoppingCartOutlined, title: 'Маркетплейсы берут 20%', desc: 'Вы работаете в убыток или задираете цены.' },
  { icon: ArrowRightOutlined, title: 'Переходы на сайты убивают конверсию', desc: 'Покупатель ушел по ссылке и не вернулся.' },
  { icon: SmileOutlined, title: 'Свой интернет-магазин сложно продвигать', desc: 'Никто не вбивает адрес вручную.' },
]
</script>