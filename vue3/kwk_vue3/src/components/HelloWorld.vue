<template>
  <div class="hello">
    <h1>{{ myData }}</h1>
    <button @click="clickHandler">修改</button>
    <button @click="clickRemove">删除</button>
  </div>
</template>

<script setup>
// 1 reactive / shallowReactive浅响应式
import { reactive } from 'vue';
const myData = reactive([1, 2, 3])
function clickHandler(){
  myData.push(10)
  
}
// 2 ref / shallowRef

function clickRemove(){
  myData.pop()
}
// 3 reanOnly 只读数据
// 4 computed
// 5 watch
// 6 watchEffect
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
