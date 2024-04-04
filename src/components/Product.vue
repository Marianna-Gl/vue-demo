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
    value: string,
    name: String,
    price: Number,
    description: String,
    fruit: Object
  }
}
</script>


<template>
    <div><Name :value="'name' />
        <Price :value='price' />
        <Description :value='description' /></div>
 
    {{ value }}

</template>
<style scoped></style>
