<script setup>
import { ref } from "vue";
import HelloWorldVue from "./components/HelloWorld.vue";

const greet = ref(true);
const count = ref(0);
</script>

<template>
  <div>
    <button @click="greet = !greet">Click me</button>

    <h1 v-if="greet">Hello, how are you?</h1>
    <h1 v-else>I'm fine, thank you.</h1>
  </div>
  <br />
  <div>
    <button @click="count++">mood counter</button>
    <p>How happy are you?: {{ count }}%</p>
  </div>
  <br />
  <div>
    <HelloWorldVue />
  </div>
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
