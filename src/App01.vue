<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1> {{msg}}</h1>
  <!--   v-once 内容只渲染一次-->
  <h1 @click="changMsg" v-once>{{msg}}</h1>
  <input type="text" v-model="msg">
  <!--   v-html 加载html指令-->
  <div>{{content}}</div>
  <div v-html="content"></div>
  <!--   v-bind 绑定属性-->
  <div :id="id" :class="id"></div>
  <div v-bind:id="id"></div>

</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      msg: 'helloword',
      content: '<h1>标题</h1><h2>标题2</h2>',
      id: 'd1'
    }
  },
  methods: {
    changMsg () {
      this.msg = '帅呆了'
      this.id = 'd2'
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
