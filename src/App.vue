<script setup lang="ts">
import { ref } from 'vue';

const foo = ref(1);
</script>

<!-- this is working fine-->
<!-- <template>
  <button @click="(foo as number)++">{{ foo }}</button>
</template> -->

<!-- this generates `Uncaught SyntaxError: Unexpected identifier 'as' at...` in HMR -->
<template lang="pug">
button(@click="(foo as number)++")
  | {{ foo }}
</template>

<style>
button {
  cursor: pointer;
  user-select: none;
}
</style>