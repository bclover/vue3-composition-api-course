<script setup>
  import { ref } from 'vue';
  import { vAutofocus } from '@/directives/vAutofocus';

  const appTitle = 'Vue 3 Counter App';
  const counter = ref(0);
  const title = ref('My Counter:'); 

  const decreaseCounter = () => {
    (counter.value > 0) ? counter.value-- : counter.value = 0;
  }

  const increaseCounter = () => {
    counter.value++;
  }
</script>

<template>
  <div class="home">
    <h2> {{  appTitle }}</h2>
    <h3> {{ title }}</h3>
    <div>
      <button class="btn" @click="decreaseCounter">-</button>
      <span class="counter">{{ counter }}</span>
      <button class="btn" @click="increaseCounter">+</button>
    </div>

    <div class="edit">
      <h3>Edit Title Here:</h3>
      <input v-model="title" type="text" v-autofocus>
    </div>
  </div>
</template>

<style>
.home {
  text-align: center;
  padding: 1em;
}

.btn {
  cursor: pointer;
    width: 1em;
}

.btn, .counter {
  font-size: 2.75em;
  margin: .25em;
}
</style>
