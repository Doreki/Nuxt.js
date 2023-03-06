<template>
  <div class="list-wrapper">
    <ul>
      <li v-for="cart in carts" :key="cart.id" class="list-item">
        <img class="thumbnail" :src="cart.imageUrl" :alt="cart.name" />
        <div class="description">
          <p>{{ cart.name }}</p>
          <span>{{ cart.price }}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import { FETCH_CART_ITEMS } from '~/store'

export default {
  name: 'NuxtCartList',
  async fetch() {
    await this.$store.dispath(FETCH_CART_ITEMS)
  },
}
</script>

<style scoped></style>
