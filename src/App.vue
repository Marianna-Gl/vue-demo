<script>
export default {
  data() {
    return {
      email: '',
      isValid: false
    };
  },
  methods: {
    openPrompt() {
      const userInput = prompt('Please enter your email');
      if (userInput !== null) {
        this.email = userInput;
        this.isValid = this.validateEmail(userInput);
      }
    },
    reset() {
      this.email = '';
      this.isValid = false;
    },
    validateEmail(email) {
      // Regular expression for basic email validation
      const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      return regex.test(email);
    }
  }
};
</script>


<template>
  <div>
    <button @click="openPrompt">Input Email</button>
    <button @click="reset">Reset</button>

    <div v-if="email">
      <h1 :style="{borderColor: isValid ? 'green' : 'red'}">{{ email }}</h1>
      <h4>{{ isValid ? 'The email is valid' : 'The email is invalid' }}</h4>
    </div>
  </div>
</template>



<style>
h1 {
  border: 2px solid;
  padding: 10px;
  display: inline-block;
}
</style>