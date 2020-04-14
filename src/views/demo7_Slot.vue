<template>
  <div id="Demo7">
    <Clock>
      <span style="color:red;">เวลาปัจจุบัน</span>
    </Clock>

    <Clock>
      <span style="color:green;">Current Time</span>
    </Clock>

    <Clock/> <!-- using fallback content -->
  </div>
</template>

<script>
import Clock from "@/components/helpers/Clock.vue";
export default {
  name: "Demo7",
  components: {
    Clock
  }
};
</script>

<style></style>
