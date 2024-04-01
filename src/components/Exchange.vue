<script>
export default {
  data() {
    return {
      usd,
      amd
    }
  }
}
//   methods:{
//     typeCurrency(event){
//         console.log(event.target.value);
//     }

//     }
</script>

<template>
  {{ Exchange }}

  <div>AMD -> USD կամ USD -> AMD</div>
  <br />
  <div>
    <input type="text" @input="typeCurrency" />
    <input type="text" @input="typeCurrency" />
  </div>
  <br /><br />
  <button @click="chooseCurrecncy">
    <!-- Display the current conversion mode -->
    <p v-if="mode === 'amd-to-usd'">Conversion Mode: AMD to USD</p>
    <p v-else>Conversion Mode: USD to AMD</p>

    <!-- Display the conversion component based on the mode -->
    <div v-if="mode === 'amd-to-usd'">
      <p>Convert AMD to USD</p>
      <!-- Your conversion component for AMD to USD -->
    </div>
    <div v-else>
      <p>Convert USD to AMD</p>
      <!-- Your conversion component for USD to AMD -->
    </div>
  </button>
</template>

<style scoped></style>
