<template>
  <div id="app">
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/demo1">demo1</router-link></li>
      <li><router-link to="/demo2">demo2 Events</router-link></li>
      <li><router-link to="/demo3">demo3 Data</router-link></li>
      <li><router-link to="/demo4">demo4 Compute</router-link></li>


    </ul>

    <router-view></router-view>
    <span class="title">123</span>
  </div>
</template>

<script>
export default {
  name: "app"
};
</script>

<style scoped>
ul {
  margin: 0;
  padding: 0;
}
li {
  display: inline;
  margin-right: 8px;
}

.title{
  font-size: 30px;
  color: purple;
}
</style>

<style>
.content{
  color:blue;
}
</style>