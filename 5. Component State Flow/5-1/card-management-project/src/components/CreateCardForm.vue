<template>
    <div>
        <form @submit.prevent="createCardFunc">
            <span class="input-box">
                <label for="name">이름 
                    <input type="text" id="name" v-model="inputName">
                </label>
            </span>
            <span class="input-box">
                <label for="title">직함 
                    <input type="text" id="title" v-model="inputTitle">
                </label>
            </span>
            <button>명함 추가</button>
        </form>
    </div>
</template>

<script setup>
import {ref} from 'vue'

const inputName = ref("")
const inputTitle = ref("")

const emit = defineEmits(["createCardEvent"])

const createCardFunc = function () {
    const cardInfo = {
        name: inputName.value,
        title: inputTitle.value

    }
    emit('createCardEvent', cardInfo)
    inputName.value = ""
    inputTitle.value = ""
}
</script>

<style scoped>
.input-box {
    margin: 10px
}
</style>