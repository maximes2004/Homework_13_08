<template>
  <div id="app">
<!-- Используем компонент ProductDetails -->
    <ProductDetails/>
  </div>
</template>

<script>
// Импортируем компонент ProductDetails
import ProductDetails from './components/ProductDetails.vue'
export default {
  name: 'App',
  components: {
    // Регистрируем компонент ProductDetails
    ProductDetails
  }
}
</script>

<style scoped>
h1 {
  font-size: 24px;
  margin-bottom: 10px;
}
p {
  font-size: 18px;
}
</style>
