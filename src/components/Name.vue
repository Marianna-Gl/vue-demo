<script>
export default {
  name: 'Name',
  props: {
    name: {
      type: String,
      required: true
    }
  }
}
</script>
<template>
  <div>
    <h2>{{ name }}</h2>
  </div>
</template>
