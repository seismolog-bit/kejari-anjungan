<template>
  <v-app>
    <Header />
    <Navigator />
    <Content />
  </v-app>
</template>

<script>
import Header from '~/components/layout/header.vue'
import Navigator from '~/components/layout/navigator.vue'
import Content from '~/components/layout/content.vue'
export default {
  components: {
    Header,
    Navigator,
    Content
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
</style>
