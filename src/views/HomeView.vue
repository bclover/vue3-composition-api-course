<script setup>
  import { ref } from 'vue';

  const counter = ref(0);

  const decreaseCounter = () => {
    (counter.value > 0) ? counter.value-- : counter.value = 0;
  }

  const increaseCounter = () => {
    counter.value++;
  }
</script>

<template>
  <div class="home">
    <div>
      <button class="btn" @click="decreaseCounter">-</button>
      <span class="counter">{{ counter }}</span>
      <button class="btn" @click="increaseCounter">+</button>
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
