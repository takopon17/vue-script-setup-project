<script lang="ts" setup>
import { ref } from "@vue/reactivity";
import NavBar from "../src/components/NavBar.vue";
const count = ref(0);
const increment = () => {
  count.value++;
};
const decrement = () => {
  count.value--;
};
</script>

<template>
  <nav-bar />
  <section class="mx-20">
    <h1>{{ count }}</h1>
    <button
      class="
        rounded
        px-3
        py-2
        bg-gray-500
        text-white
        hover:bg-gray-300
        active:bg-slate-700
        mr-4
      "
      @click="increment"
    >
      Increment
    </button>
    <button
      class="
        rounded
        px-3
        py-2
        bg-gray-500
        text-white
        hover:bg-gray-300
        active:bg-slate-700
        mr-4
      "
      @click="decrement"
    >
      Decrement
    </button>
  </section>
</template>
