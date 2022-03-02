<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h1 v-if="user=='超级vip'">欢迎金主爸爸</h1>
    <h1 v-else-if="user=='vip'">欢迎会员</h1>
    <h1 v-else>充值更强大</h1>
    <button @click="toggleUser">vip过期</button>
    <!--    设置1个内容切换显示-->
    <h1 v-show="isShow">切换显示内容</h1>
    <button @click="toggleShow">切换</button>
  </div>
</template>
<script>

export default {
  name: 'App',
  data () {
    return {
      user: 'vip',
      isShow: true
    }
  },
  methods: {
    toggleUser: function () {
      this.user = '普通用户'
    },
    toggleShow: function () {
      this.isShow = !this.isShow
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
