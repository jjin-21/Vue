<template>
  <div class="q">
    <header>
      <div class='card'>
        <h1>명함 관리 페이지</h1>
      </div>
    </header>

    <main>
      <p>명함을 관리하는 페이지입니다. 여기에 명함 목록이 표시됩니다.</p>
    </main>

    <article>
      <BusinessCard />
    </article>

    <footer>
      <p>2023 My Business Cards</p>
    </footer>
  </div>
</template>

<script setup>
import BusinessCard from './components/BusinessCard.vue';
</script>

<style scoped>
header, main, article {
  text-align: center;
}
footer {
  text-align: center;
  background-color: lightgray;
  padding-top: 10px;
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