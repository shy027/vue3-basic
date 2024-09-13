<template>
    <div>
        <!-- <button v-bind="isDisable">点击</button> -->
        <button :disabled="isDisable">点击</button>
        <img :src="url" src="" />
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const isDisable = ref<boolean>(false)
const url = ref<string>('https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1qgLQ2.img?w=640&h=359&m=6')
</script>

<style scoped>

</style>