<template>
  <div class="home">
    <div>
      <button class="btn" @click="decreaseCounter">-</button>
      <span class="counter">{{ counter }}</span>
      <button class="btn" @click="increaseCounter">+</button>
    </div>
  </div>
</template>

<script>
  import { ref } from 'vue';
  export default {

    setup() {

      const counter = ref(0);

      const decreaseCounter = () => {
        (counter.value > 0) ? counter.value-- : counter.value = 0;
      }

      const increaseCounter = () => {
        counter.value++;
      }
    
      return {
        counter, decreaseCounter, increaseCounter
      }

    }
  }
</script>
<style>
.home {
  text-align: center;
  padding: 1em;
}

.btn {
  cursor: pointer;
}

.btn, .counter {
  font-size: 2.75em;
  margin: .25em;
}
</style>
