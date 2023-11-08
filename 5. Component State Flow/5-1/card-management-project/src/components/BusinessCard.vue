<template>
    <div>
        <h3>보유 명함 목록</h3>
        <div>
            <p>현재 보유중인 명함 수 : </p>
        </div>
        <div class="card">
            <BusinessCardDetail v-for="card in cardInfos" :key="card" 
            :info="card"
            @delete-card="deleteCard"
            />
        </div>
    </div>
</template>

<script setup>
import BusinessCardDetail from './BusinessCardDetail.vue';
import {ref} from 'vue'

const cardInfos = ref([
    {name: '일론 머스크', title: '테슬라 테크노킹'},
    {name: '래리 엘리슨', title: '오라클 창업주'},
    {name: '빌 게이츠', title: '마이크로소프트 창업주'},
    {name: '래리 페이지', title: '구글 공동창업주'},
    {name: '세르게이 브린', title: '구글 공동창업주'},
])

const deleteCard = function(info) {
    const cardIndex = cardInfos.value.findIndex((card)=>{ 
            return card.name === info.name && card.title === info.title
        })
        console.log(cardIndex)
        if (cardIndex !== -1) {
            cardInfos.value.splice(cardIndex,1)
        }
}
</script>

<style scoped>
.card {
    display: inline-block;
}
</style>