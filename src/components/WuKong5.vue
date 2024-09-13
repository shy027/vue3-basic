<!--
 * @Author: shy 1533103845@qq.com
 * @Date: 2024-09-10 12:51:22
 * @LastEditors: shy 1533103845@qq.com
 * @LastEditTime: 2024-09-10 13:10:31
 * @FilePath: \vue3-basic\src\components\WuKong5.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
    <div class="d1">
        <div class="d2">
             基础攻击力：
             <input v-model="baseAttack" type="number" />
        </div>
        <div class="d3">
            装备加成：
            <input v-model="gearBonus" type="number" />
        </div>
        <p>总攻击力：{{ totalAttack}}</p>
    </div>
</template>

<script setup lang="ts">
import {computed,ref} from 'vue'
const baseAttack = ref<number>(50)
const gearBonus = ref<number>(20)
const totalAttack = computed(() =>{
  return  baseAttack.value + gearBonus.value
})
</script>

<style scoped>
.d1{
    margin: auto;
    background-color: rgba(0,0,0,0.1);
    text-align: center;
    border-radius: 5px;
    box-shadow:  0 4px 8px rgba(0,0,0,0.1);
    padding-top: 10px;
    padding-bottom: 10px;
    width: 500px;
    padding-bottom: 30px;
}
.d2,.d3,p{
    margin: auto;
    font-size: 30px;
    width: 420px;
    margin-top: 20px;
    border-radius: 5px;
}
input{
    text-align: center;
    margin: auto;
    font-size: 30px;
    width: 300px;
    margin: 10px;
    border-radius: 5px;
    box-shadow:  0 4px 8px rgba(0,0,0,0.1);
}
</style>