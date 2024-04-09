<script>
import Name from './Name.vue'
import Price from './Price.vue'
import Description from './Description.vue'

export default {
  components: {
    Name,
    Price,
    Description
  },
  props: {
    fruit: {
      type: Object,
      required: true
    }
  },
  methods: {
    submitCur() {
      this.$emit('submitCur', this.price)
    }
  }
}
</script>

<template>
  <div class="product">
    <Name :name="fruit.name" />
    <Price :price="fruit.price" />
    <Description :description="fruit.description" />
  </div>
</template>
