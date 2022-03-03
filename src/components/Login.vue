<template>
    <div>
      <input type="text" v-model="username">
      <button @click="sendMsg">将数据提交到父组件</button>
    </div>
</template>


<script>
export default {
  data:function () {
    return{
      username:''
    }
  },
  methods:{
    sendMsg:function (){
      //触发自定义事件,$emit(事件名称，发送事件的参数)
      this.$emit('sendParentMsg',this.username)
    }
  }
}
</script>
