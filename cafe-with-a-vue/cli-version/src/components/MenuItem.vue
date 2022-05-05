<template>
  <div>
    <img class="menu-item__image" :src="image.source" :alt="image.alt" />
    <h3>{{ name }}</h3>
    <p v-if="inStock">In Stock</p>
    <p v-else>Out of Stock</p>
    <label for="add-item-quantity">Quantity: {{ quantity }}</label>
    <input v-model.number="quantity" id="add-item-quantity" type="number" />
    <button @click="addToShoppingCart(quantity)">Add to Shopping Cart</button>
  </div>
</template>

<script>
export default {
  name: "MenuItem",
  props: ["image", "name", "inStock", "quantity", "addToShoppingCart"],
};
</script>

<style>
</style>