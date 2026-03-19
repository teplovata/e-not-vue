<template>
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl md:text-4xl font-bold text-center text-gray-900 mb-10">
        Для кого это
      </h2>
      <div class="grid md:grid-cols-3 gap-6">
        <div v-for="(niche, index) in niches" :key="index" 
             class="text-center p-6 border rounded-xl hover:shadow-lg transition">
          <div class="mb-4 flex justify-center">
            <component :is="niche.icon" class="text-4xl" :class="niche.color" />
          </div>
          <h3 class="text-xl font-semibold mb-2">{{ niche.title }}</h3>
          <p class="text-gray-600">{{ niche.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { 
  CoffeeOutlined, 
  SkinOutlined, 
  ShoppingOutlined 
} from '@ant-design/icons-vue'

const niches = [
  { 
    icon: CoffeeOutlined, 
    color: 'text-orange-500', 
    title: 'Рестораны и кафе', 
    desc: 'Сбор предзаказов, доставка.' 
  },
  { 
    icon: SkinOutlined, 
    color: 'text-pink-500', 
    title: 'Розничные магазины', 
    desc: 'Одежда, косметика, товары для дома.' 
  },
  { 
    icon: ShoppingOutlined, 
    color: 'text-green-500', 
    title: 'Локальный бизнес', 
    desc: 'Цветы, сувениры, фермерские продукты.' 
  },
]
</script>