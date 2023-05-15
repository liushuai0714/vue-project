<template>
    <span>我是子组件 --msg:{{ msg }}</span>
</template>

<script setup>
import { ref } from "vue"
const msg = ref("this is a msg from child conponent")
const m1 = () =>{
    console.log("this is method m1 at child component");
    
}
//默认不暴露子组件的数据
//暴露后父组件才可以获取到数据
defineExpose({
    msg,
    m1
})
</script>