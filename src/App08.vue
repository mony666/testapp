<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <ol>
      <li v-for="(item,index) in news " :key='index'>{{item}}-->{{index}}</li>
    </ol>
    <ol>
      <li v-for="(item,index) in news1 " :key='index'>{{item.title}}-->{{item.num}}-->{{item.tag}}-->{{index}}</li>
    </ol>
    <ol>
      <li v-for="(item,index) in laochen " :key='index'>{{item}}-->{{index}}</li>
    </ol>
  </div>
</template>
<script>

export default {
  name: 'App',
  data () {
    return {
      news: [
        '“两会时间”即将开启',
        '外媒：基辅电视塔附近爆炸致5死',
        '公安部开展打击拐卖妇幼犯罪行动',
        '俄外长发言时多国外交官退场',
        '拜登：普京在战事上“严重失算”'
      ],
      news1: [
        {
          title: '外媒：基辅电视塔附近爆炸致5死',
          tag: '沸',
          num: '450万'
        },
        {
          title: '公安部开展打击拐卖妇幼犯罪行',
          tag: '沸',
          num: '450万'
        },
        {
          title: '拜登：普京在战事上“严重失算”',
          tag: '沸',
          num: '450万'
        }
      ],
      laochen: {
        name: '老陈',
        age: 30,
        type: '帅'
      }
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
