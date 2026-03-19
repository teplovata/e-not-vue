<template>
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row items-center gap-8 max-w-3xl mx-auto">
        <div class="w-40 h-40 rounded-full overflow-hidden shadow-lg flex-shrink-0 border-4 border-blue-100">
          <img 
            :src="photo" 
            alt="Полина - основатель e-not"
            class="w-full h-full object-cover"
          />
        </div>
        <div>
          <p class="text-lg text-gray-700 leading-relaxed">
            «Я — Полина. 7 лет в маркетинге, знаю, как бесят потери клиентов и высокие комиссии. 
            Ушла из найма, выучила код и с поддержкой мужа-программиста написала идеальный инструмент 
            для продаж в мессенджерах. Сама подключаю, сама поддерживаю, сама отвечаю за результат».
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import photo from '../assets/photo.jpeg' 
</script>