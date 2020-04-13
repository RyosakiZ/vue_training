<template>
  <div id ="demo4">

    <h2>{{firstname}}</h2>
    <h2>{{lastname}}</h2>
    <h2>{{fullname}}</h2>

    <h1 style="background-color: grey;">
      Random No. from computed property: {{ getrandomno }}
    </h1>
        <h1 style="background-color: grey;">
      Random No. from computed property: {{ getrandomno }}
    </h1>
        <h1 style="background-color: grey;">
      Random No. from computed property: {{ getrandomno }} 
      <!-- ดึงค่าล่าสุดเสมอ (เปลี่ยนทุกค่าที่คิดก่อนหน้า เลยทำให้ค่าเหมือนกัน) -->
    </h1>
    <h1>Random No from method: {{ getrandomno1() }}</h1>
    <h1>Random No from method: {{ getrandomno1() }}</h1>
    
  </div>
</template>

<script>
export default {
  name: "Demo4",
  methods:{
    getrandomno1: function() {
      return Math.random();
    }
  },
  data(){
    return{
    firstname: "Puwit",
    lastname: "Chotikasatian"
    }
  },
  computed:{
    fullname(){
      return this.firstname + " " + this.lastname
    },
    getrandomno(){
      return Math.random();
    }
  }
}
</script>