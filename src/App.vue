<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import {ref} from 'vue'
let count= ref(0);
let secondCount=ref(0);
function increment(){
count.value++;
}
function decrement(){
count.value--;
}
function decrementByTen(){
   count.value= count.value-10;
}
function incrementByTen(){
count.value= count.value+10;
}
function reset(){
  count.value=0;
}

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />

    <button @click="decrementByTen()">-10</button>
    <button @click="decrement()">-1</button>
    <span>{{ count}}</span>
    <button @click="increment()">+1</button>
     <button @click="incrementByTen()">+10</button>
    <button @click="reset()">reset</button>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
