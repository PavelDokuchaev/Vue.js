<template>
  <div>
    <h2>Товар: {{ product.name }}</h2>
    <h2>Цена: {{ formattedPrice }}</h2>
    <h2 class="in" v-if="product.available">Available</h2>
    <h2 class="out" v-else>Out of stock</h2>
  </div>
</template>

<script>
export default {
  props: {
    product: Object,
  },
  computed: {
    formattedPrice() {
      return '$' + this.product.price;
    }
  }
}
</script>

<style lang="scss" scoped>
div {
  border: 2px solid #000;
  width: 200px;
}

.in {
  color: green;
}

.out {
  color: red;
}
</style>