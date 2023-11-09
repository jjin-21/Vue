<template>
    <div class="quiz-box">
        <p><strong>{{ info.pk }}번 문제. {{ info.question }}</strong></p>
        <p><label for="answer">정답 입력 </label></p>
        <input type="text" name="answer" id="answer">
    </div>
</template>

<script setup>
const props = defineProps({
    info: Object
})
</script>

<style scoped>
.quiz-box {
    display: inline-block;
    background-color: rgb(240, 240, 240);
    border: 1px solid lightgray;
    margin: 10px;
    border-radius: 10px;
    width:85%;
    padding: 30px;
    padding-top: 5px;
}
label {
    font-size: 13px;
}
input {
    width: 90%; /* 너비 설정 */
    height: 30px; /* 높이 설정 */
}
</style>