<!--
 * @Author: shy 1533103845@qq.com
 * @Date: 2024-09-10 10:26:25
 * @LastEditors: shy 1533103845@qq.com
 * @LastEditTime: 2024-09-10 10:37:45
 * @FilePath: \vue3-basic\src\components\WuKong3.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
    <div>
        <h2>技能列表</h2>
        <ul>
            <li v-for="skill in skills" :key="skill.id">
                {{skill.name}} - 
                <span v-if="skill.status == true" class="y">已解锁</span>
                <span v-else class="n">未解锁</span>
            </li>
        </ul>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
interface Skill{
    id: number
    name: string
    status: boolean
}
const skills = ref<Skill[]>([
    {id: 1,name: '定身术',status: true},
    {id: 2,name: '聚形散气',status: true},
    {id: 3,name: '身外身法',status: true},
    {id: 4,name: '铜头铁臂',status: false},
])
</script>

<style scoped>
div{
    margin: auto;
    background-color: rgba(0,0,0,0.2);
    text-align: center;
    border-radius: 5px;
    box-shadow:  0 4px 8px rgba(0,0,0,0.1);
    padding-top: 10px;
    padding-bottom: 10px;
    width: 500px;
}
.y{
    color: green;
}
.n{
    color: red;
}
ul li {
    list-style: none;
}
</style>