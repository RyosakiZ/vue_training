<template>
  <div id="demo3">
    <h1>Data</h1>
    <button @click="count++;isLogged=true;">Count++</button>
    <span>{{ count }}</span>
    <div>{{ message }}</div>
    <div>{{ isLogged }}</div>
    <input type="text" placeholder="Enter a message" v-model="message" />
    <h2 v-if="isLogged">Yahooo</h2>
    <div>{{account.username}} {{account.password}}</div>
    <div>{{courses[0]}}</div>
    <ul>
      <li class="content" v-for="(item, index) in courses" :key="index">{{index+1}}. {{item}}</li>
    </ul>

    <span class="title">5555</span>
  </div>
</template>

<script>
export default {
  name: "Demo3",
  mounted() {
    this.message = "Welcome to CodeMobiles";
  },
  data() {
    return {
      count: 0,
      message: "",
      isLogged: false,
      account: {
        username: "admin",
        password: "1234"
      },
      courses:[
        "Angular",
        "VueJS",
        "ReactJS",
        "Flutter",
        "UX/UI"
      ]
    };
  }
};
</script>

<style>

li{
  color: red
}

.title{
  color: brown
}
</style>

<style>

</style>