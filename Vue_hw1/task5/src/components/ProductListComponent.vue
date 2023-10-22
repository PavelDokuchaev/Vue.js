<template>
  <div>
    <ProductDetailsTwoComponent v-for="product in products" :key="product.id" :product="product" />
  </div>
</template>

<script>
import ProductDetailsTwoComponent from './ProductDetailsTwoComponent.vue';

export default {
  data() {
    return {
      products: [
        {
          id: 1,
          name: 'Карась',
          price: 80,
          available: true
        },
        {
          id: 2,
          name: 'Окунь',
          price: 150,
          available: false
        },
        {
          id: 3,
          name: 'Судак',
          price: 200,
          available: true
        },
        {
          id: 4,
          name: 'Сом',
          price: 100,
          available: true
        }
      ]
    };
  },
  components: { ProductDetailsTwoComponent }
}
</script>

<style lang="scss" scoped>
div {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
</style>