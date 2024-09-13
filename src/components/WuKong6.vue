<!--
 * @Author: shy 1533103845@qq.com
 * @Date: 2024-09-11 14:13:11
 * @LastEditors: shy 1533103845@qq.com
 * @LastEditTime: 2024-09-11 14:31:34
 * @FilePath: \vue3-basic\src\components\WuKong7.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AEim
-->
<template>
    <div class="d1">
        <h1>装备栏</h1>
        <div class="d2">
            <input v-model="newEquip" />
            <button @click="addEquip">添加装备</button>
        </div>
            <ul>
                <li v-for="(item,index) in equip" :key="index">
                    {{ item }} 
                    <button @click="deleteEquip(index)">删除</button>
                </li>
            </ul>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const equip = ref<string[]>([])
const newEquip = ref()
const addEquip = () => {
    equip.value.push(newEquip.value)
    newEquip.value = ''
}
const deleteEquip = (index) => {
    equip.value.splice(index,1)
}
</script>

<style scoped>
.d1 {
    max-width: 600px;
    margin: 0 auto;
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.d2{
    text-align: center;
}
h1 {
    text-align: center;
    color: #333;
    margin-bottom: 20px;
}

input{
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    margin-right: 20px;
    width: 200px; 
    height: 20px;
}

button {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    margin: 10px;
}

button:hover {
    background-color: #0056b3;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    text-align: center;
    padding: 10px;
    margin-top: -1px; 
    justify-content: space-between;
    align-items: center;
    height: 50px;
}

li:first-child {
    border-top-left-radius: 4px;
    border-top-right-radius: 4px;
}

li:last-child {
    border-bottom-left-radius: 4px;
    border-bottom-right-radius: 4px;
}
.delete-button {
    background-color: #ff4d4d;
    color: white;
    border: none;
    border-radius: 4px;
    padding: 5px 10px;
    cursor: pointer;
}

.delete-button:hover {
    background-color: #cc0000;
}
</style>