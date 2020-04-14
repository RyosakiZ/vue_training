<template>
  <div id="Clock">
    <slot>Now</slot> : {{time}}
  </div>
</template>

<script>
import moment from "moment";
export default {
    name: "Clock",
    data() {
        return {
            time: ""
        }
    },
    mounted() {
        setInterval(() => {
            this.time = moment(Date()).format('MM/DD/YYYY hh:mm:ss')
        }, 1000);
    },

}
</script>

<style>

</style>