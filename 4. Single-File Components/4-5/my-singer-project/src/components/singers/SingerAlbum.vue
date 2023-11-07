<template>
    <div class="album-info">
        <p class="song-title"><strong>앨범 제목</strong></p>
        <p class="song" v-for="song in songs">{{ song }}</p>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const songs = ref(['노래 목록 1','노래 목록 2','노래 목록 3'])
</script>

<style scoped>
.album-info {
    display: inline-block;
    border-radius: 10px; /* 모서리를 둥글게 만드는 값 (픽셀) */
    border: 1px solid #ccc;
    background-color: lightgray;
    width: 35%;
    margin: 20px;
}
.song-title {
    margin: 5px;
}
.song {
    color: coral;
}
</style>