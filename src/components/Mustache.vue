<!--
 * @Author: shy 1533103845@qq.com
 * @Date: 2024-09-10 08:42:25
 * @LastEditors: shy 1533103845@qq.com
 * @LastEditTime: 2024-09-10 08:48:08
 * @FilePath: \vue3-basic\src\components\Mustache.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
    <div>
        <h2>
            当期用户： {{username}}
        </h2>
        <p>2+3的结果是：{{2+3}}</p>
        <p>全名：{{firstName + lastName}}</p>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const username = ref<string>('张三')
console.log(username.value);
const firstName = ref<string>('张')
const lastName = ref<string>('三')
</script>

<style scoped>

</style>