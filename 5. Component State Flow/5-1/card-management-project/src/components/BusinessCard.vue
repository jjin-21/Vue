<template>
    <div>
        <h3>보유 명함 목록</h3>
        <div>
            <p v-if="cardInfos.length>0">현재 보유중인 명함 수 : {{ cardInfos.length }}</p>
            <p v-else>명함이 없습니다. 새로운 명함을 추가해 주세요.</p>
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
import {ref, watch} from 'vue'

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
        if (cardIndex !== -1) {
            cardInfos.value.splice(cardIndex,1)
        }
}

const props = defineProps({
    newinfo: Object
})

watch(props.newinfo, (card) => {
    cardInfos.value.push(card)
}) 
</script>

<style scoped>
.card {
    display: inline-block;
}
</style>