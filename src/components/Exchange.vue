<script>
export default {
  data() {
    return {
      formattedIrp: null,
      mode: 'AMD',
      amount: '',
      disabled: true,
      numberInput: null,
      updatedValue: null
    }
  },

  methods: {
    toggleMode() {
      this.mode = this.mode === 'AMD' ? 'USD' : 'AMD'
    },
    updateValue() {
      if (this.numberInput !== null && this.mode !== 'AMD') {
        this.updatedValue = this.numberInput * 400
      } else {
        this.updatedValue = this.numberInput / 400
      }
    }
  }
}
</script>

<template>
  {{ Exchange }}

  <div>
    <h1 class="a">{{ mode === 'AMD' ? 'AMD -> USD' : 'USD -> AMD' }}</h1>
    <div>
      <input v-model="numberInput" @input="updateValue" />
      <input :value="updatedValue" :disabled="disabled" />
    </div>

    <button @click="toggleMode" class="bb">
      {{ mode !== 'AMD' ? 'AMD -> USD' : 'USD -> AMD' }}
    </button>
  </div>
</template>

<style scoped>
.bb {
  padding-right: 47px;
  padding-left: 50px;
  padding-top: 10px;
  padding-bottom: 10px;
  margin-top: 7px;
}
.a {
  color: blue;
}
</style>
