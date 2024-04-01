<script>
export default {
  data() {
    return {
      mode: 'AMD', // Initial mode
      amount: '' // Input value
    }
  },
  methods: {
    toggleMode() {
      this.mode = this.mode === 'AMD' ? 'USD' : 'AMD'
    }
  }
}
</script>

<template>
  {{ Exchange }}

  <div>
    <h2>{{ mode === 'AMD' ? 'AMD -> USD' : 'USD -> AMD' }}</h2>
    <div>
      <input type="text" @input="typeCurrency" />
      <input type="text" @input="typeCurrency" />
    </div>
    <!-- <input type="text" v-model="amount" /> -->
    <button @click="toggleMode">{{ mode !== 'AMD' ? 'AMD -> USD' : 'USD -> AMD' }}</button>
  </div>

  <!-- Display the current conversion mode -->
  <!-- <p v-if="mode === 'amd-to-usd'">Conversion Mode: AMD to USD</p>
    <p v-else>Conversion Mode: USD to AMD</p> -->

  <!-- Display the conversion component based on the mode -->
  <!-- <div v-if="mode === 'amd-to-usd'">
      <p>Convert AMD to USD</p> -->
  <!-- Your conversion component for AMD to USD -->
  <!-- </div>
    <div v-else>
      <p>Convert USD to AMD</p> -->
  <!-- Your conversion component for USD to AMD -->
  <!-- </div>
  </button>
  -->
</template>

<style scoped></style>
