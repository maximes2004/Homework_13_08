<template>
    <div>
      <!-- Отображаем название продукта -->
      <h1>{{ product.name }}</h1>
      <!-- Отображаем форматированную цену продукта -->
      <p>Price: {{ formattedPrice }}</p>
      <!-- Проверяем доступность продукта и отображаем соответствующее сообщение -->
      <p>Status: {{ product.available ? 'Available' : 'Out of stock' }}</p>
    </div>
</template>
<script>
export default {
// Название компонента
  name: 'ProductDetails',
  // Данные компонента
  data () {
    return {
    // Объект product, представляющий информацию о продукте
      product: {
        name: 'Sample Product', // Название продукта
        price: 99.99, // Цена продукта
        available: true // Доступность продукта
      }
    }
  },
  // Вычисляемые свойства
  computed: {
    // Вычисляемое свойство для форматированной цены продукта
    formattedPrice () {
      // Возвращаем цену, форматированную с знаком доллара и двумя десятичными знаками
      return `$${this.product.price.toFixed(2)}`
    }
  }
}
</script>
<style scoped>
  /* Стилизация компонента */
  h1 {
    font-size: 24px;
    margin-bottom: 10px;
  }
  p {
    font-size: 18px;
  }
</style>
