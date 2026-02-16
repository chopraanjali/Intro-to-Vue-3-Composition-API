<script setup>
import { ref } from 'vue' //state management
// ref is a function that takes an initial value and returns a reactive reference to that value.

const product = ref('Socks')
</script>

<template>
  <div class="product-display">
    <div class="product-container">
      <div class="product-info">
        <h1>{{ product }}</h1>
      </div>
    </div>
  </div>
</template>