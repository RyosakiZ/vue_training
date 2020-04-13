<template>
  <div id="demo5">
    <img v-bind:src="imageUrl" v-bind:height="height" />
    <br />
    <a :href="link">My Website</a>
    <div :class="[false ? error : '',important]">CodeMobiles</div>
    <div :style="{color, fontSize}">Binding Style</div>
    <div :style="isActive ? styleObj: ''">Binding Style Obj</div>
    <button @click="isActive = !isActive">ToggleActive</button>

  </div>
</template>

<script>
export default {
  name: "Demo5",
  data() {
    return {
      imageUrl: "https://www.mk1642.com/MKDelivery/media/Source/logo.png",
      height: 50,
      link: "https://www.mk1642.com",
      error: "error_class",
      important: "important",
      color: "green",
      fontSize: "30px",
      styleObj:{
        backgroundColor: "yellow",
        color: "green"
      },
      isActive: false
    };
  }
};
</script>

<style>
.error_class{
  background-color: red;
  color: white;
}

.important{
  font-weight: 900;
}
</style>
