<!--
 * @Author: shy 1533103845@qq.com
 * @Date: 2024-09-10 09:25:14
 * @LastEditors: shy 1533103845@qq.com
 * @LastEditTime: 2024-09-10 09:36:51
 * @FilePath: \vue3-basic\src\components\SunChange.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
    <div>
        <h2>{{name}}</h2>
        <h3>当前形态：{{title}}</h3>
        <button @click="changeTitle">切换形态</button>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const name = ref<string>('孙悟空')
const title = ref<string>('斗战胜佛')
const changeTitle = () =>{
    if(title.value == '齐天大圣'){
       title.value = '斗战胜佛'
    }else{
        title.value = '齐天大圣'
    }
}
</script>

<style scoped>
div {
    margin: auto;
    background-color: yellow;
    text-align: center;
    border-radius: 5px;
    box-shadow:  0 4px 8px rgba(0,0,0,0.1);
    padding-top: 20px;
    padding-bottom: 20px;
    width: 1000px;
}
button{
    background-color: red;
    padding: 5px;
    color: white;
}
button:hover{
    cursor:pointer;
}
</style>