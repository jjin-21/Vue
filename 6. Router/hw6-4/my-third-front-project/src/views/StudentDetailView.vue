<template>
    <div>
        <h1>학생 상세 정보 페이지입니다.</h1>
        <p>이름 :  {{ name }}</p>
    </div>
</template>

<script setup>
import { useRoute, useRouter } from 'vue-router';
const route = useRoute()

const name = route.params.name
</script>

<style scoped>

</style>