<template>
  <div class="max-w-4xl mx-auto">
    <h1 class="text-4xl font-bold text-center mb-8">Привет! Мы — Братва 👊</h1>
    
    <div class="prose prose-lg mx-auto">
      <p class="text-lg mb-6">
        Мы — обычные первокурсники из Козыбаева, учимся в Северном Казахстане.
        Нас пятеро: Амина, Нурдаулет, Ералы, Адлет и Аружан.
      </p>

      <p class="text-lg mb-6">
        Назвали себя "Братва", потому что мы реально команда — поддерживаем друг друга, 
        шутим, учимся, делаем проекты и просто вместе проходим через всё, что даёт 
        студенческая жизнь.
      </p>

      <p class="text-lg mb-6">
        На этом сайте будем выкладывать наши идеи, проекты и, может быть, немного 
        весёлых историй из жизни :)
      </p>

      <p class="text-lg font-semibold text-center">
        Заходи, будет интересно!
      </p>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'default'
})
</script>

<style>
.prose {
  max-width: 65ch;
  color: #374151;
}

.prose p {
  margin-top: 1.25em;
  margin-bottom: 1.25em;
}
</style> 