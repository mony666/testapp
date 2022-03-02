<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!--计算属性-->
  <div class="d1">{{msg.split('').reverse().join('')}}</div>
  <div :id='reverseMsg' class="d1">{{reverseMsg}}</div>

  <p>Has published books:</p>
  <span>{{ publishedBooksMessage }}</span>
  <p>{{now}}</p>
  <!--  监听事件-->
  <input type="text" v-model="msg">
  <h1>{{msg}}</h1>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      msg: 'helloworld',
      author: {
        name: 'John Doe',
        books: [
          'Vue 2 - Advanced Guide',
          'Vue 3 - Basic Guide',
          'Vue 4 - The Mystery'
        ]
      }

    }
  },
  // 计算属性
  computed: {
    reverseMsg: function () {
      return this.msg.split('').reverse().join('')
    },
    publishedBooksMessage () {
      return this.author.books.length > 0 ? 'Yes' : 'No'
    },
    now () {
      return Date.now()
    }
  },
  methods: {
    toggleColor: function () {
      this.attributeName = 'id'
    }
  },
  // 监听值的变化
  watch: {
    msg: function (newValue, oldValue) {
      if (newValue.length < 10) {
        console.log('newValue', newValue)
        console.log('oldValue', oldValue)
        alert('输入的值太少了！')
      }
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
