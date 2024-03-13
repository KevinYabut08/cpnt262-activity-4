<script>
// use of props to generate the slot
export default {
  props: ["content"],
};
</script>

<template>
  <div class="card">
    <slot></slot>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.card {
  max-width: 250px;
  text-align: center;
  margin: 2rem;
  padding: 0.6rem 0.8rem;
  border: 0.1rem solid beige;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
