<script setup>
import { ref } from 'vue'
import socksGreenImage from './assets/images/socks_green.jpeg'

const product = ref('Socks')
const image = ref(socksGreenImage)
const inventory = ref(5)
const onSale = ref(true)

</script>
  
<template>
  <div class="nav-bar"></div>
  <div class="product-display">
    <div class="product-container">
      <div class="product-image">    
        <img v-bind:src="image">
      </div>
      <div class="product-info">
        <h1>{{ product }}</h1>
        <p v-if="inventory > 10">In stock</p>
        <p v-else-if="inventory >0 && inventory <= 10">Only few items left!</p>
        <p v-else>Out of stock</p>
        <p v-if="onSale">On Sale!</p>
      </div>
    </div>
  </div>
</template>