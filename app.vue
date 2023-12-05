<script setup>
const config = useRuntimeConfig()
const title = 'DriveGo Electric'
const description = 'The ultimate course for mastering State Management with Pinia by Eduardo San Martin Morote, the author of Pinia. Order now for an early access discount.'

useServerSeoMeta({
  title,
  ogTitle: title,
  description,
  ogDescription: description,
  ogImage: `${config.public.APP_ROOT}/images/meta-3.png`,
  twitterCard: 'summary_large_image'
})
</script>


<template>
  <div>
    <NuxtPage />
  </div>
</template>
