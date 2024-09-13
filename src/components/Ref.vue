<!--
 * @Author: shy 1533103845@qq.com
 * @Date: 2024-09-10 10:08:02
 * @LastEditors: shy 1533103845@qq.com
 * @LastEditTime: 2024-09-10 10:08:09
 * @FilePath: \vue3-basic\src\components\Ref.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
    <div>
        <P>当前计数：{{count}}</P>
        <button @click="increment">增加计数</button>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const count = ref<number>(0)
const increment = (): void =>{
    count.value++;
}
</script>

<style scoped>

</style>