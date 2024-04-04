<script>
export default {
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
