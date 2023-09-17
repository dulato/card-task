<template>
  <div class="app">
    <div class="main">
      <div class="container">
        <div class="content">
          <my-cards></my-cards>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MyCards from './components/MyCards.vue'

export default {
  name: 'App',
  components: {
    MyCards
  }
}
</script>

<style lang="scss">
  @import "@/assets/styles/style.scss"
</style>
