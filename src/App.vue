<script setup>
import qiz from './data/quizes.json';
import {ref, watch} from 'vue';

const quizes = ref(qiz);
const searchInput = ref('');

watch(searchInput, ()=>
  quizes.value = qiz.filter(quiz => quiz.name.toLowerCase().includes(searchInput.value.toLowerCase()))
)
</script>

<template>
  <div class="container">
    <header>
      <h1>Quizes</h1>
      <input v-model.trim="searchInput" type="text" placeholder="search...">
    </header>
  <div class="cards-container">
    <div class="card" v-for="quiz in quizes" :key="quiz.id">
      <img :src="quiz.img" alt=""/>
      <div class="card-text">
        <h2> {{ quiz.name }} </h2>
        <p> {{ quiz.questions.length }} Questions </p>
      </div>
    </div>
  </div>
  </div>
</template>

<style scoped>
.container{
  max-width: 1000px;
  margin: 0 auto;
}

header{
  margin-top: 30px;
  margin-bottom: 10px;
  display: flex;
  align-items: center;
}

header h1 {
  font-weight: bold;
  margin-right: 30px;
}

header input{
  border: none;
  background-color: rgba(255, 255, 255, 0.737);
  border-radius: 5px;
  padding: 5px;
}

.cards-container{
  display: flex;
  flex-wrap: wrap;
  margin-top: 30px;
}

/* CARD */
.card{
  width: 310px;
  overflow: hidden;
  border-radius: 3%;
  box-shadow: 1px 1px 1px rgb(62, 61, 61);
  margin-bottom: 35px;
  margin-right: 20px;
  cursor: pointer;
}

.card img{
  width: 100%;
  height: 190px;
  margin: 0;
}

.card .card-text{
  padding: 0 5px;
}

.card .card-text h2{
  font-weight: bold;
}
</style>