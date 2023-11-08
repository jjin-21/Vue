<template>
  <div class="q">
    <header>
      <div class='card'>
        <h1>명함 관리 페이지</h1>
      </div>
    </header>

    <main>
      <p>명함을 관리하는 페이지입니다. 여기에 명함 목록이 표시됩니다.</p>
      <CreateCardForm @create-card-event="updateCard" />
    </main>

    <article>
      <BusinessCard :newinfo="newCard" />
    </article>

    <footer>
      <p>2023 My Business Cards</p>
    </footer>
  </div>
</template>

<script setup>
import CreateCardForm from './components/CreateCardForm.vue';
import BusinessCard from './components/BusinessCard.vue';
import {ref} from 'vue'

const newCard = ref({
  name: "",
  title: ""
})
const updateCard = function(newinfo) {
  newCard.value.name = newinfo.name,
  newCard.value.title = newinfo.title
}

</script>

<style scoped>
header, main {
  text-align: center;
}
article {
  text-align: center;
  padding-bottom: 50px;
}
footer {
  text-align: center;
  background-color: lightgray;
  margin-top: 10px;
  position: fixed;
  bottom: 0;
  width: 100%;
}
.card {
  display: inline-block;
  text-align: center;
  color: white;
  background-color: rgb(31, 128, 189);
  width: 50%;
  padding: 15px;

}
</style>