<template>
    <card class="singer-info">
        <h1>가수 이름</h1>
        <img class="singer" src="@/assets/singer.jpg" alt="singer">
        <p>가수 소개글</p>
    </card>
</template>

<script setup>

</script>

<style scoped>
.singer-info {
    border: 1px solid black;
    display: inline-block;
    width: 40%;
    margin: 20px;
}

.singer {
    border-radius: 50%; /* 50%의 원형 모양으로 이미지 출력 */
    width: 200px;
    height: 200px;
}
</style>