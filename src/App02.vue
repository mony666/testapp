<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!--  javascript 表达式可以在模板语法使用-->
  <h1> {{msg.split('')}}</h1>
  <h1> {{msg.split('').reverse()}}</h1>
  <h1> {{msg.split('').reverse().join('')}}</h1>
  <div :id="msg.split('').reverse().join('')" :class="id"></div>
  <div>{{color=='green'?'开心':'难过'}}</div>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      msg: 'helloword',
      color: 'yellow'
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#d1 {
   width: 100px;
   height: 100px;
   background: red;
 }
#d2 {
  width: 100px;
  height: 100px;
  background: green;
}
</style>
