<template>
  <div class="font-sans antialiased">
    <Header 
      @showDemo="showDemo"
      @openForm="formVisible = true" />
    
    <main>
      <Hero @openForm="formVisible = true" />
      <Problem />
      <Solution @showDemo="showDemo" />
      <KillerFeature />
      <HowItWorks />
      <ForWhom />
      <Pricing />
      <About />
      
      <!-- Блок призыва к действию -->
      <section class="py-16 bg-gradient-to-b from-blue-600 to-indigo-700 text-white">
        <div class="container mx-auto px-4 text-center">
          <h2 class="text-3xl md:text-4xl font-bold mb-4">
            Готовы продавать там, где ваши клиенты?
          </h2>
          <p class="text-lg opacity-90 mb-8">
            Оставьте заявку, и мы в течение дня подключим ваш магазин.
          </p>
          <a-button 
            type="primary"
            size="large"
            @click="formVisible = true"
            class="bg-white text-blue-600 hover:bg-gray-100 border-none h-12 px-8 text-base font-semibold"
          >
            Хочу попробовать
          </a-button>
        </div>
      </section>
    </main>

    <Footer />

    <!-- Модальное окно с формой -->
    <ContactForm
      v-model:visible="formVisible"
      @submit="handleFormSubmit"
    />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { message } from 'ant-design-vue'
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Problem from './components/Problem.vue'
import Solution from './components/Solution.vue'
import KillerFeature from './components/KillerFeature.vue'
import HowItWorks from './components/HowItWorks.vue'
import ForWhom from './components/ForWhom.vue'
import Pricing from './components/Pricing.vue'
import AboutMe from './components/AboutMe.vue'
import Footer from './components/Footer.vue'
import ContactForm from './components/ContactForm.vue'

const formVisible = ref(false)

const showDemo = () => {
  message.info('Демо-версия скоро будет доступна!')
}

const handleFormSubmit = (formData) => {
  // Здесь будет отправка данных
  console.log('Form submitted:', formData)
  message.success(`Спасибо, ${formData.name}! Мы свяжемся с вами.`)
}
</script>