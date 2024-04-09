<script>
export default {
  props: {
    price: {
      type: String,
      required: true
    }
  },
  computed: {
    convertedPrice() {
      if (this.currency === 'USD') {
        return this.price;
      } else {
        // Assuming 1 USD = 400 AMD
        return (parseFloat(this.price) * 400).toFixed(2) + ' ֏';
      }
    }
  },
  data() {
    return {
      currency: 'USD'
    };
  },
  methods: {
    toggleCurrency() {
      this.currency = this.currency === 'USD' ? 'AMD' : 'USD';
      this.$emit('toggleCurrency');
    }
  }
};
</script>

<template>

  <div>
    <span>{{ convertedPrice }}</span>
    <button @click="toggleCurrency">Change the currency</button>
  </div>
</template>
