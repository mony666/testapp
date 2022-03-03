<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <!--    绑定事件，不需要参数-->
    <h1 @click="toggle">{{msg}}</h1>
    <!--    绑定事件，直接处理表达式-->
    <h1 @click="msg+=1">{{msg}}</h1>
    <!--    绑定事件，传递参数-->
    <h1 @click="toggle1(10)">{{msg}}</h1>
    <!--    event事件对象-->
    <!--    绑定事件，传递事件对象和参数-->
    <h1 @click="toggle2(10,$event)">{{msg}}</h1>
    <h1 v-on:@click="toggle2(10,$event)">{{msg}}</h1>
    <!--    一个事件绑定多个对象-->
    <h1 :style="{background:color}" @click="toggle2(10,$event),addcolor()">{{msg}}</h1>
    <!--    事件修饰符-->
    <!--  阻止事件冒泡.stop
          阻止默认事件.prevernt
          事件只会触发一次.once
     -->
    <h1 v-on:@click.once="toggle2(10,$event)">{{msg}}</h1>
    <!--    按键修饰符-->
    <input type="text" @keydown.enter="searchEvent">

  </div>
</template>
<script>

export default {
  name: 'App',
  data () {
    return {
      msg: 0,
      color: 'red'
    }
  },
  methods: {
    toggle: function (event) {
      console.log(event)
      this.msg += 1
    },
    toggle1: function (number) {
      this.msg += number
    },
    // event 事件对象
    toggle2: function (number, event) {
      console.log(event)
      this.msg += number
    },
    addcolor: function () {
      this.color = 'green'
    },
    searchEvent: function () {
      console.log('执行了回车的搜索事件')
    }
  }
}
</script>

<style>
#app {
  /*font-family: Avenir, Helvetica, Arial, sans-serif;*/
  /*-webkit-font-smoothing: antialiased;*/
  /*-moz-osx-font-smoothing: grayscale;*/
  /*text-align: center;*/
  /*color: #2c3e50;*/
  /*margin-top: 60px;*/
}
.active{
  background: #42b983;
}
</style>
