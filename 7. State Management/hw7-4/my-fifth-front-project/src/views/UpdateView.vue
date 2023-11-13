<template>
    <div>
        <h2>데이터 수정 페이지</h2>
        <p>이름: {{ info.name }}</p>
        <p>잔고: {{ info.balance }}</p>
        <button @click="moreMoney">+</button>
    </div>
</template>

<script setup>
import { useRoute, useRouter } from 'vue-router';
import { useBalanceStore } from '@/stores/balance'

const route = useRoute()
const balance = useBalanceStore()
const info = balance.search(route.params.name)

const moreMoney = () => {
    info.balance += 1000
}
</script>

<style scoped>

</style>