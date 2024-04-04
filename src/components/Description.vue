<script>
export default {
  name: 'Description',
  props: {
    description: {
      type: String,
      required: true
    }
  }
};
</script>

<template>
  <div>
    <p>{{ description }}</p>
  </div>
</template>