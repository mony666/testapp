<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!--动态指令-->
  <div v-bind:[attributeName]="d1"></div>
  <div :[attributeName]="d1"></div>
  <button @click="toggleColor">点击切换颜色</button>
  <button @[eventName]="toggleColor">点击切换颜色</button>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      attributeName: 'class',
      d1: 'd1',
      eventName: 'click'
    }
  },
  methods: {
    toggleColor: function () {
      this.attributeName = 'id'
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
.d1 {
  width: 100px;
  height: 100px;
  background: green;
}
</style>
