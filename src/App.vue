<script>
import chartComponent from './components/chart-component.vue'
import fontsComponent from './components/font-component.vue'
export default {
  name: 'App',
  components: {
    chartComponent,
    fontsComponent,
  },
}
</script>
<template>
  <chartComponent></chartComponent>
</template>
<style lang="scss">
@import '@/assets/colors.scss';
body{
  width: 100%;
  background-color: $cream;
}
</style>
