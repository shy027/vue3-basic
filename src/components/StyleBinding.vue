<!--
 * @Author: shy 1533103845@qq.com
 * @Date: 2024-09-10 09:05:29
 * @LastEditors: shy 1533103845@qq.com
 * @LastEditTime: 2024-09-13 10:46:36
 * @FilePath: \vue3-basic\src\components\StyleBinding.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
    <div>
        <p :style="pStyle">这是一段有样式的文字</p>
        <button @click="toggleStyle">切换样式</button>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'

const  isBold = ref<boolean>(false)
const pStyle = ref<{
    fontWeight: string
    color: string
}>({
    fontWeight: 'normal',
    color: 'black',
})

const toggleStyle = () =>{
    isBold.value = !isBold.value
    pStyle.value = {
        fontWeight: isBold.value ? 'bold' : 'normal',
        color: isBold.value ? 'blue' : 'black',
    }
}
</script>

<style scoped>

</style>