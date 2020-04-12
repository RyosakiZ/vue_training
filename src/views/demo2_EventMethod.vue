<template>
  <div app="demo2">
    <h1>Event and Method</h1>
    <button v-on:click="clickMe">Click Me</button>
    <button v-on:click="clickMe2('Welcome to VueJS')">Click Me 2</button>
    <button @click="clickMe3('Welcome to CodeMobiles')">Click Me 3</button>
  </div></template
>

<script>
export default {
  name: "Demo2",
  methods: {
    clickMe() {
      alert("Hi");
    },
    clickMe2(message) {
      alert(message);
    },
    clickMe3(message) {
      alert(message);
    },
  },
};
</script>

<style></style>
