<template>
    <div class="center-content">
        <h1>가수 목록</h1>
        <SingerDetail v-for="singer in singers"/>
    </div>
</template>

<script setup>
import SingerDetail from './singers/SingerDetail.vue';
import { ref } from 'vue';

const singers = ref([{name: 'adele'},
                    {name: 'maroon 5'},
                    {name: 'Dua Lipa'}])
</script>

<style scoped>
h1 {
    color: orange;
}
.center-content {
    text-align: center;
}
</style>