<script setup>
import { ref } from "vue";
// code for data-binding
const message = ref("");

// code for event handling
const name = ref("User");

function greet(event) {
  alert(`Hello ${name.value}!`);
  if (event) {
    alert(event.target.tagName);
  }
}
</script>

<template>
  <div>
    <button @click="greet">Greet</button>
  </div>
  <div>
    <p>Message is: {{ message }}</p>
    <input v-model="message" placeholder="please be nice :)" />
  </div>
</template>
