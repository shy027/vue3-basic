<!--
 * @Author: shy 1533103845@qq.com
 * @Date: 2024-09-13 10:29:23
 * @LastEditors: shy 1533103845@qq.com
 * @LastEditTime: 2024-09-13 10:32:48
 * @FilePath: \vue3-basic\src\components\MethodsNoArg.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
    <div>
        <p>当前温度: {{temperature}}℃</p>
        <button @click="increaseTemp">增加温度</button>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const temperature = ref<number>(20)
const increaseTemp = (): void =>{
    temperature.value++
}
</script>

<style scoped>

</style>