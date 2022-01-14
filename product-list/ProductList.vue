<template>
  <div>
     <p>{{products}}</p>
      <ProductCard v-bind:singleProduct="product" v-for="product in products" v-bind:key="product.productId"/>
  </div>
</template>

<script>
import ProductCard from './ProductCard.vue'
export default {
    components:{ ProductCard},
 props:[ 'products']
}
</script>

<style>

</style>