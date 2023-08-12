<template>
  <div class="container">
    <header>
      <h1>Quizes</h1>
      <input type="text" placeholder="search...">
    </header>
  <div class="cards-container">
    <div class="card">
      <img src="https://i0.wp.com/calmatters.org/wp-content/uploads/2021/08/math-curriculum.jpg?fit=2000%2C1500&ssl=1" alt=""/>
      <div class="card-text">
        <h2>Math</h2>
        <p>15 Questions</p>
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
  border-radius: 2%;
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