<template>
    <div class="child-box">
        <h3>자식 페이지입니다.</h3>
        <p>이름 : {{ props.info.name }}</p>
        <p>나이 : {{ props.info.age }}</p>
        <p>용돈 : {{ props.info.balance }}</p>
        <button @click="giveMeAllowance">용돈 주세요.</button>
    </div>
</template>

<script setup>
const props = defineProps({
    info: Object
})

const emit = defineEmits(['moreMoney'])
const giveMeAllowance = function () {
    emit('moreMoney', props.info)
}
</script>

<style scoped>
.child-box {
    border: 1px solid gray;
    margin: 15px;
    padding: 5px;
}
</style>