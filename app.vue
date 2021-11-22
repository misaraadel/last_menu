<template>
<div>
  <NuxtPage />
</div>
</template>

<script setup lang="ts">
  const title = 'المنيو'
  const description = 'بدات خدمات المنيو.كوم في عام ٢٠٠٧ وهدفنا هو تأسيس وتطوير مطاعم الوجبات السريعة من البداية الي النجاح، من خلال فريق متخصص في إدارة وتشغيل مطاعم الوجبات السريعة والكوفي شوب'

  useMeta({
	  title: title,

    htmlAttrs: { lang: 'ar', dir: 'rtl' },

    link: [{ rel: 'icon', type: 'image/png', href: '/icon.png' }],

    meta: [
      { hid: 'description', name: 'description', content: description },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { hid: 'google', name: 'google', content: 'notranslate' }
    ]
  })
</script>
