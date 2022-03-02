<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <!--    类class-->
    <!--    第一种写法，放置字符串-->
    <h1 :class="msg">hello1</h1>
    <!--    第二种写法，放置对象-->
    <h1 :class="{active:isActive}">hello2</h1>
    <button @click="toggleActive">点击切换Active</button>
    <!--    第三种写法，放置数组-->
    <h1 :class="arr">hello3</h1>
    <!--    第四种写法，数组和对象的结合-->
    <h1 :class="['classname4', {active:isActive}]">hello4</h1>

  </div>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      msg: 'background:yello',
      isActive: true,
      arr: ['swiper', 'active'],
      classname4: 'abc'
    }
  },
  methods: {
    toggleActive: function () {
      this.isActive = !this.isActive
      this.arr.pop()
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


