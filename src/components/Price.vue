<script>
export default {
  name: 'Price',
  props: {
    price: {
      type: String,
      required: true
    }
  }
}
</script>

<template>
  <div>
    <p>{{ price }}</p>
  </div>
</template>
