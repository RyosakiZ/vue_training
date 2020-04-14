<template>
  <div id="header">
    <ul>
      <li><router-link to="/"><button>Home</button></router-link></li>
      <li><router-link to="/demo1"><button>Demo1 Intro</button></router-link></li>
      <li><router-link to="/demo2"><button>Demo2 Events</button></router-link></li>
      <li><router-link to="/demo3"><button>Demo3 Data</button></router-link></li>
      <li><router-link to="/demo4"><button>Demo4 Compute</button></router-link></li>
      <li><router-link to="/demo5"><button>Demo5 Binding</button></router-link></li>
      <li><router-link to="/demo6"><button>Demo6 Form & V-Model</button></router-link></li>
      <li><router-link to="/demo7"><button>Demo7 Slot</button></router-link></li>
    </ul>
  </div>
</template>

<script>
export default {
    name: "Header"
}
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

</style>
