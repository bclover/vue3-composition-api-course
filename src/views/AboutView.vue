<script setup>
  import { vAutofocus } from '@/directives/vAutofocus';
</script>

<template>
  <div class="about">
    <h1>About</h1>
  </div>
  <div class="edit">
      <h3>Test Autofocus Directive:</h3>
      <input v-model="autofocusInput" type="text" v-autofocus>
  </div>
</template>
