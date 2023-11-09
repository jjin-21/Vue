<template>
    <div class="create-box">
        <h2>퀴즈 생성</h2>
        <form @submit.prevent="createQuiz(problemInput, answerInput)">
            <div>
                <p><label for="problem">문제</label></p>
                <textarea name="problem" id="problem" cols="70" rows="7" v-model="problemInput"></textarea>
            </div>
            <div>
                <p><label for="answer">답안</label></p>
                <input class="answer-box" type="answer" name="answer" id="answer" v-model="answerInput">
            </div>
            <button type="submit" class="btn">퀴즈 생성</button>
        </form>
    </div>
</template>

<script setup>
import {ref} from 'vue'

const quizObj = ref({problem: '', answer: ''})
const problemInput = ref("")
const answerInput = ref("")
const createQuiz = function(problem, answer) {
    console.log(quizObj)
    quizObj.value.problem = problem
    quizObj.value.answer = answer
    problemInput.value = ""
    answerInput.value = ""
    console.log(quizObj)
}
</script>

<style scoped>
.create-box {
    display: inline-block;
    background-color: rgb(240, 240, 240);
    padding: 25px;
    margin: 30px;
    width: 57%;
    border-radius: 10px;
}
.answer-box {
    width: 96%;
    height: 30px;
}
.btn {
    color: white;
    margin-top: 13px;
    width: 97.5%;
    height: 40px;
    background-color: rgb(59, 125, 248);
    border-radius: 7px;
    border : 1px solid rgb(59, 125, 248);
}
</style>