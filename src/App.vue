<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <div>
      <p>Array = {{ item }}</p>
      <p>Buy = {{minVal}}</p>
      <p>Sell = {{maxVal}}</p>
      <p>benefit = {{benefit}}</p>
      <button @click="myFunction()">Click Me</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Vue Test',
      item:[7, 3, 9, 5, 6, 4],
      maxVal:'',
      minVal:'',
      benefit:''
    }
  },
  methods : {
    myFunction: function () {
      this.maxVal = Math.max.apply(Math, this.item);
      this.minVal = Math.min.apply(Math, this.item);
      this.benefit = this.maxVal - this.minVal;

    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
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
