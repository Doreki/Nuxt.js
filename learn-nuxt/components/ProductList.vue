<template>
  <div>
    {{ products }}
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'NuxtProductList',
  async asyncData({ params, $http }) {
    const res = await axios.get('http://localhost:3000/products')
    const products = res.data
    return { products }
  },

  data() {
    return {}
  },

  mounted() {},

  methods: {},
}
</script>

<style lang="scss" scoped></style>
