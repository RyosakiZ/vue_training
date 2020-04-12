<template>
<div>
  <!-- interpolation -->
  <h1>{{title}}</h1>
  <h2>{{count}}</h2>
  <!-- <button @click="count++">Add</button> -->
  <button @click="onClickAdd">Add</button>
</div>
</template>

<script>
export default {
  name:"app",
  data() {
    return {
      title:"CodeMobile www.codemobiles.com",
      count:0
    }
  },
  methods: {
    onClickAdd(){
      this.count++
    }
  },
};
</script>

<style>
</style>
