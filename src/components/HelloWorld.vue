<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div>
      <p>{{val}}</p>
      <button v-on:click='updateMethod'>Click to Update/Before Update</button>
    </div>
    <div>
      <p>Life cycle methods of vue js</p>
      <ol>
        <li>beforeCreate</li>
        <li>created</li>
        <li>beforeMount</li>
        <li>mounted</li>
        <li>beforeUpdate</li>
        <li>updated</li>
        <li>beforeDestroy</li>
        <li>destroyed</li>
      </ol>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      val: 0,
    }
  },
  methods:{
    updateMethod(){
      this.val++;
    },
  },
  created: function () {
    console.log("Created")
  },
  beforeCreate: function () {
    alert("open console")
    console.log("Before created")
  },
  mounted: function () {
    console.log("Mounted")
  },
  beforeMount: function () {
    console.log("Before mounted")
  },
  updated: function () {
    console.log("Updated val: " + this.val)
  },
  beforeUpdate: function () {
    console.log("Before updated val: " + this.val)
  },
  destroyed: function () {
    console.log("Destroyed ")
  },
  beforeDestroy: function () {
    console.log("Before destroyed ")
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
