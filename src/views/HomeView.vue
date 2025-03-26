<script setup>

</script>

<template>
  <div class="home">
    <div>
      <button class="btn" @click="decreaseCounter">-</button>
      <span class="counter">{{  counter }}</span>
      <button class="btn" @click="increaseCounter">+</button>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      counter: 0
    }
  },

  methods: {
    decreaseCounter() {
      (this.counter > 0) ? this.counter-- : this.counter = 0;
    },
    increaseCounter() {
      this.counter++;
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
