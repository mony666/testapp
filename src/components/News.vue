<template>
  <div>
      <h1>新闻内容: {{content}} </h1>
      <h1>从父组件获取到的值：{{msg}}</h1>
  </div>
</template>

<script>
export default {
  props: ['content','msg']
}
</script>
