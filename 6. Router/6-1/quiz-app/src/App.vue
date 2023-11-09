<template>
  <div>
    <div class="quiz">
      <div class="quiz-des">
        <h1 class="quiz-top">Quiz 퀴즈</h1>
        <p class="quiz-mid">여기는 퀴즈의 나라! 지금 바로 도전해보세요!</p>
        <nav class="quiz-bot">
          <RouterLink class="text-first" :to="{name: 'home'}">Home</RouterLink>
          <RouterLink class="text" :to="{name: 'quiz'}">Quiz</RouterLink>
        </nav>
      </div>
    </div>
    <div>
      <RouterView />
    </div>
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<style scoped>
.quiz {
  display: flex;
  justify-content: center;
}
.quiz-des {
  background-color: rgb(239, 239, 239);
  text-align: center;
  padding:10px;
  width: 60%;
}
.quiz-top {
  background-color: orange;
  color: white;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  margin: 10px;
  margin-bottom: 0px;
  padding: 20px;
}
.quiz-mid {
  background-color: white;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  margin: 10px;
  margin-top: 0px;
  padding: 60px;
}
.quiz-bot {
  color: white;
  background-color: rgb(65, 65, 65);
  padding: 8px;
  margin: 10px;
  margin-top: 40px;
}
.text-first {
  color: white;
  text-decoration: none; /* 하이퍼링크 밑줄 제거 */
  padding: 0px 10px;
}
.text {
  color: white;
  text-decoration: none; /* 하이퍼링크 밑줄 제거 */
  border-left: 1px solid white;
  padding: 0px 10px;
}
</style>