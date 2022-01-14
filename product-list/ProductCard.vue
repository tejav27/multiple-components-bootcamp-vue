<template>
  <div>
<p>Product Id::{{singleProduct.productId}}</p>
<p>Name::{{singleProduct.productName}}</p>
<p>Price::{{singleProduct.productPrice}}</p>
<p>rating:: {{singleProduct.rating}}</p>
<img v-bind:src="singleProduct.productImage" alt="">
  </div>
</template>

<script>
export default {
 props:[ 'singleProduct']
    
}
</script>

<style>

</style>