<template>
    <div>
        <h1>학생 정보 페이지입니다.</h1>
        <p v-for="student in students">
            <a @click="goDetail(student.name)">{{ student.name }} 학생 정보 보기</a>
        </p>
    </div>
</template>

<script setup>
import { useRoute, useRouter } from 'vue-router';
import {ref} from 'vue'

const students = ref([
    {name: '김하나'},
    {name: '김두리'},
    {name: '김서이'}
])

const router = useRouter()

const goDetail = function(stuName) {
    router.push({name: "studentdetail", params: {name: stuName}})
}
</script>

<style scoped>
a {
  text-decoration: none; /* 하이퍼링크 밑줄 제거 */
  cursor: pointer; /* 커서를 포인터로 변경 */
}

a:hover {
   text-decoration: underline; /* 마우스를 올리면 밑줄 표시 */
}
</style>