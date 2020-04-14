<template>
  <div id="app">
    <Header />
    <!-- <ul>
      <li><router-link to="/"><button>Home</button></router-link></li>
      <li><router-link to="/demo1"><button>Demo1 Intro</button></router-link></li>
      <li><router-link to="/demo2"><button>Demo2 Events</button></router-link></li>
      <li><router-link to="/demo3"><button>Demo3 Data</button></router-link></li>
      <li><router-link to="/demo4"><button>Demo4 Compute</button></router-link></li>
      <li><router-link to="/demo5"><button>Demo5 Binding</button></router-link></li>
      <li><router-link to="/demo6"><button>Demo6 Form & V-Model</button></router-link></li>
    </ul> -->
    <!-- <div class="content-wrapper">
    <router-view></router-view>
    </div> -->
    <Content />
    <Footer @onClock="onClock" title="Copyright 2020 by Puwit Chotikasatian Ltd." color="black"/>
    <div class="clock">{{time}}</div>
    <!-- <span class="footer">Copyright 2020 by Puwit Chotikasatian</span> -->

  </div>
</template>

<script>
import Header from "@/components/layout/Header.vue"
import Content from "@/components/layout/Content.vue"
import Footer from "@/components/layout/Footer.vue"
import moment from "moment";

export default {
  name: "app",
  methods: {
    onClock(value){
      // this.time = value
      this.time = moment(value).format('MM/DD/YYYY hh:mm:ss')
    }
  },
  data(){
    return{
      time: ""
    }
  },
  components: {
    Header,
    Content,
    Footer
  }
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
  font-size: 15px;
  color: grey;
}

.clock{
  font-size: 12px;
}

</style>

<style>
.content{
  color:blue;
}
</style>