<template lang="pug">
  v-app.app-wrapper
    v-app-bar(app dark)
      v-container
        v-row
          v-col(md="6")
            v-btn.logo-btn(color="primary" to="/" large)
            template(
              v-for="item in menu"
            )
              v-btn.ml-3(
                :to="item.to"
                :key="item.to"
                large
                text
              ) {{ item.title }}
            v-btn.ml-3(icon)
              v-icon mdi-magnify
          v-col(grow)
          v-col.text-right(md="3")
            v-btn(icon)
              v-icon mdi-bell
            v-btn(icon)
              v-icon mdi-login
    v-container.content
      v-main
        nuxt
    v-container
      app-footer
</template>

<script>
import AppFooter from '~/components/AppFooter'
export default {
  components: {
    AppFooter,
  },
  data() {
    return {
      menu: [
        { to: '/blog', title: 'Кейсы' },
        { to: '/publ', title: 'Уроки' },
        { to: '/tests', title: 'Тесты' },
      ],
    }
  },
}
</script>
<style scoped>
.app-wrapper {
  background-color: #dedede;
}
.content {
  background: #fff;
  min-height: calc(100vh - 50px);
}
.logo-btn {
  background-image: url('/logo.png');
  background-repeat: no-repeat;
  margin-left: 0px;
  width: 90px;
  background-position: 40%;
}
</style>
