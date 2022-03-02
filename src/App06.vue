<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <!--    style样式-->
    <!--    第一种写法，放置字符串-->
    <h1 :style="msg">hello1</h1>
    <!--    第二种写法，放置对象-->
    <h1 :style="{toggleActive:'purple'}">hello2</h1>
    <button @click="toggleActive">点击切换Active</button>
    <h1 :style="styleObj">hello3</h1>
    <!--    第四种写法，数组和对象的结合-->
    <h1 :style="[styleObj,{width:'500px'}]">hello4</h1>

  </div>
</template>
<script>

export default {
  name: 'App',
  data () {
    return {
      msg: 'background: yellow;',
      styleObj: {
        'background-color': 'pink',
        border: '1px solid blue',
        boxSizing: 'border-box'

      }
    }
  },
  methods: {
    toggleActive: function () {
      this.styleObj['background-color'] = 'skyblue'
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
.active{
  background: #42b983;
}
</style>
