<template>
  <div>
    <Headers></Headers>
    <Main></Main>
    <Footer></Footer>
    <!--通过props传递子组件数据-->
    <News :content="newsContent" :msg="msg"></News>
    <!--子组件传递数据给父组件，自定义事件-->
    <Login @sendParentMsg="getChildMsg"></Login>
    <h1>从子组件获取到的值：{{msg}}</h1>

  </div>
</template>
<script>
import Headers from './components/Headers.vue'
import Footer from './components/Footer.vue'
import Main from './components/Main.vue'
import News from './components/News.vue'
import Login from  './components/Login.vue'
export default {
  name: 'App',
  data () {
    return {
      newsContent: '振兴中华',
      msg: ''
    }
  },
  methods: {
    getChildMsg:function (value) {
      console.log(value)
      this.msg = value
    }
    },
  components: {
    Headers,
    Footer,
    Main,
    News,
    Login
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
