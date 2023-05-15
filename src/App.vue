<template>
  <div>
    <h2 @click="clickEvent">我是父组件</h2>
    <Child ref="son"/>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Child from './pages/Child.vue'
const son = ref(null)
function clickEvent(){
  console.log("click here");
  console.log(son.value.msg);
  son.value.m1()
}
</script>


