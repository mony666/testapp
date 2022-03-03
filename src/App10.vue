<template>
  <div>
    <!--文本框-->
    <input v-model="searchKey" type="text" @keydown.enter="searchEvent">
    <h1>{{searchKey}}</h1>
    <textarea v-model="lineText" name="textarea" id="" cols="30" rows="10"></textarea>
    <h1>{{lineText}}</h1>
    <!--表单获取是否选中状态-->
    <input type="checkbox" name="like" v-model="checked" value="123">
    <h1>{{checked}}</h1>
    <!--复选多个值的情况-->
    <input type="checkbox" name="likes" v-model="fruits" value="苹果">
    <input type="checkbox" name="likes" v-model="fruits" value="雪梨">
    <input type="checkbox" name="likes" v-model="fruits" value="香蕉">
    <input type="checkbox" name="likes" v-model="fruits" value="葡萄">
    <h1> {{fruits}}</h1>
    <!--单选框-->
    <input type="radio" name="sex" v-model="picked" value="sex">
    <input type="radio" name="sex" v-model="picked" value="man">
    <input type="radio" name="sex" v-model="picked" value="women">
    <h1>{{picked}}</h1>
    <!--选项框-->
    <select v-model="city" name="city">
      <option value="广州">广州</option>
      <option value="上海">上海</option>
      <option value="北京">北京</option>
      <option value="深圳">深圳</option>
    </select>
    <h1>{{city}}</h1>
    <!--选项框 多选-->
    <select v-model="citys" name="city" multiple>
      <option value="广州">广州</option>
      <option value="上海">上海</option>
      <option value="北京">北京</option>
      <option value="深圳">深圳</option>
    </select>
    <h1>{{citys}}</h1>
    <!--   获取表单选中内容 -->
    <input type="checkbox" name="like" v-model="fruits1" true-value="喜欢" false-value="不喜欢">
    <h1>{{fruits1}}</h1>
    <!--修饰符-->
    <!--.lazy/从input时间变成change时间改变值-->
    <input v-model.lazy="searchKey" type="text" @keydown.enter="searchEvent">
    <h1>{{searchKey}}</h1>
    <!--number修饰符转为数字-->
    <input v-model.lazy.number="searchKey" type="text" @keydown.enter="searchEvent">
    <h1>{{searchKey}}</h1>
    <!--trim修饰符去掉空格-->
    <input v-model.lazy.trim="searchKey" type="text" @keydown.enter="searchEvent">
    <h1>{{searchKey}}</h1>
  </div>
</template>
<script>

export default {
  name: 'App',
  data () {
    return {
      searchKey: '百度一下',
      lineText: '',
      checked: false,
      fruits: [],
      picked: '',
      city: '',
      citys: [],
      fruits1: ''
    }
  },
  methods: {
    searchEvent: function () {
      console.log(this.searchKey)
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
