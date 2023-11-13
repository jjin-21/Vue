<template>
    <div v-for="info in balance.balances">
        <p>{{ info.name }}</p>
        <p>{{ info.balance }}</p>
        <button @click="goDetail(info.name)">updateBalance</button>
    </div>
</template>

<script setup>
import {useBalanceStore} from '@/stores/balance'
import { useRoute, useRouter } from 'vue-router';

const balance = useBalanceStore()
const router = useRouter()
const goDetail = function(name) {
    router.push({name: 'update', params:{name: name}})
}

</script>

<style scoped>
button {
    border-radius: 3px;
    background-color: skyblue;
}
</style>