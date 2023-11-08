<template>
    <div class="child-box">
        <h3>자식 페이지입니다.</h3>
        <p>이름 : {{ props.info.name }}</p>
        <p>나이 : {{ props.info.age }}</p>
    </div>
</template>

<script setup>
const props = defineProps({
    info: Object
})

</script>

<style scoped>
.child-box {
    border: 1px solid gray;
    margin: 15px;
}
</style>