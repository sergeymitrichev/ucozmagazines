<template lang="pug">
  div.body-2
    span 2011 - {{ year }}
    nuxt-link.mx-2(to="/") uCozMagazines.ru
    nuxt-link(to="/index/0-2") О нас
    nuxt-link.mx-2(to="/donate") Поддержать проект
</template>
<script>
export default {
  data: () => ({
    year: new Date().getFullYear(),
  }),
}
</script>
