<template>
  <section class="bg-gradient-to-b from-blue-50 to-white py-12 md:py-20">
    <div class="container mx-auto px-4">
      <div class="grid md:grid-cols-2 gap-10 items-center">
        <div>
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold leading-tight text-gray-900">
            Продавайте в Telegram, MAX и VK <br />
            <span class="text-blue-600">без комиссий и потери клиентов.</span>
          </h1>
          <p class="text-lg text-gray-600 mt-4">
            Ваш интернет-магазин внутри любимых мессенджеров. Один клик — и заказ оформлен, покупатель не уходит из чата.
          </p>
          <div class="mt-8">
            <a-button 
              type="primary"
              size="large"
              @click="$emit('openForm')"
              class="bg-blue-500 hover:bg-blue-600 text-base h-auto py-3 px-8"
            >
              <template #icon><RocketOutlined /></template>
              Попробовать бесплатно
            </a-button>
          </div>
        </div>
        <div class="bg-gray-200 rounded-2xl shadow-xl overflow-hidden border-4 border-white aspect-square md:aspect-video flex items-center justify-center">
          <div class="text-center p-4">
            <ShopOutlined class="text-6xl text-gray-400" />
            <p class="text-gray-500 mt-2 font-medium">Скриншот / гифка</p>
            <p class="text-sm text-gray-400">Интерфейс магазина</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { RocketOutlined, ShopOutlined } from '@ant-design/icons-vue'

defineEmits(['openForm'])
</script>