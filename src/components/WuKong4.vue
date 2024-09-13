<!--
 * @Author: shy 1533103845@qq.com
 * @Date: 2024-09-10 10:53:57
 * @LastEditors: shy 1533103845@qq.com
 * @LastEditTime: 2024-09-10 12:47:06
 * @FilePath: \vue3-basic\src\components\WuKong4.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
    <div class="d1">
        <span>血量：{{hp}}/300({{hpPercent}}%)</span>
        <div class="under">
            <div class="green" v-if="hpPercent>= 60" :style="{width: hpLength}"></div>
            <div class="yellow" v-else-if="hpPercent < 60 && hpPercent >=20" :style="{width: hpLength}"></div>
            <div class="red" v-else :style="{width: hpLength}"></div>
        </div>
    </div>
</template>

<script setup lang="ts">
import{ref,computed} from 'vue'
const hp = ref<number>(30)
const hpPercent = computed(() => {
    return hp.value/300*100
})
const hpLength = computed(() =>{
    return hp.value/300*500 + 'px'
})
</script>

<style scoped>
.d1{
    margin-top: 100px;
    text-align: center;
}
span{
    font-size: larger;
}
.under{
    height: 30px;
    width: 500px;
    background-color: grey;
    margin: auto;
    margin-top: 30px;
}
.green{
    background-color: green;
    height: 30px;
}
.yellow{
    background-color: yellow;
    height: 30px;
}
.red{
    background-color: red;
    height: 30px;
}
</style>