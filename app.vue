<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup>
useHead({
  script: [
    {
      src: 'https://www.googletagmanager.com/gtag/js?id=G-K8CXRRNFLL',
      async: true
    },
    {
      innerHTML: `
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());
        gtag('config', 'G-K8CXRRNFLL');
      `
    }
  ]
})
</script>
