<template>
    <div>
        <h4>이름 : {{ props.info.name }}</h4>
        <p>직함 : {{ props.info.title }}</p>
        <button @click="deleteCardEvent">명함 삭제</button>
    </div>
</template>

<script setup>
const props = defineProps({
    info: Object,
})

const emit = defineEmits(['deleteCard'])
const deleteCardEvent = function() {
    emit('deleteCard', props.info)
}
</script>

<style scoped>
div {
    border: 1px solid gray;
    display: inline-block;
    width: 400px;
    border-radius: 10px;
    margin: 10px;
    padding: 10px;
    background-color: rgb(240, 240, 240);
}
</style>