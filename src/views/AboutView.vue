<script setup lang="ts">
import { ref, onMounted, defineProps } from "vue";
// const input = ref(null);
// const about = ref(null);
// onMounted(() => {
//   input.value.focus();
//   console.log(input);
//   console.log(about.value.innerHTML);
// });
let s: string | number = 1;
console.log(s.toFixed(2));
interface Props {
  foo: string;
  bar: number;
}
const props = defineProps<Props>();
console.log(props);
const year = ref<string | number>("2020");
year.value = 2020;
</script>
<template>
  <div class="about" ref="about">
    <h1>This is an about page</h1>
    <input ref="input" />
    {{ (s as number).toFixed(2) }}
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
