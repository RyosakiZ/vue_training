<template>
  <div id="demo6">
    <form style="margin-top:20px" v-on:submit.prevent="submit">
      <!-- Firstname -->
      <div>
        <label for="first_name">Firstname: </label>
        <input type="text" name="first_name" v-model.trim="applicant.first_name" />
      </div>
      <!-- Lastname -->
      <div>
        <!-- lazy only done when user focus other box -->
        <label for="last_name">Lastname: </label>
        <input type="text" name="last_name" v-model.trim="applicant.last_name" />
      </div>
      <!-- Sex -->
      <div>
        Sex: 
        <label for="sex">Male</label>
        <input type="radio" name="sex" value="male" v-model="applicant.sex" />
        <label for="sex">Female</label>
        <input type="radio" name="sex" value="female" v-model="applicant.sex" />
      </div>
      <!-- Age -->
      <div>
        <label for="age">Age: </label>
        <input type="number" v-model.number="applicant.age">
      </div>
      <!-- Courses -->
      <div>
        Course: 
        <!-- name must be matches with data, otherwise it will not autochoose -->
        <select name="courses" v-model="applicant.courses"> 
          <option value="react">React</option>
          <option value="angular">Angular</option>
          <option value="vuejs">VueJS</option>
        </select>
      </div>

      <button type="button" @click.exact="clear" @click.alt="useDefault">Clear</button> 
      <button type="submit">Submit</button>
      
    </form>

    <div style="margin-top:16px; color:red;">
      #Spy {{ JSON.stringify(applicant) }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Demo6",
  data() {
    return {
      applicant: {
        first_name: "",
        last_name: "",
        sex: "male",
        age: 18,
        courses: "react"
      }
    };
  },
  methods: {
    submit(){
      // event.preventDefault();
      alert(JSON.stringify(this.applicant))
    },
    clear(){
      this.applicant = {
        first_name: "",
        last_name: "",
        sex: "male",
        age: 0,
        courses: "react"
      }
    },
    useDefault(){
      this.applicant = {
        first_name: "UNKNOWN",
        last_name: "UNKNOWN",
        sex: "male",
        age: 10,
        courses: "react"
      }
    }
  },
};
</script>

<style></style>
