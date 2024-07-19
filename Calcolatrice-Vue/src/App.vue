<script setup lang="ts"></script>

<template>
  <div class="container">
    <div class="upper-box">
      <div id="schermo">0</div>
    </div>

    <div class="lower-box">
      <div class="left-box">
        <div class="calc-row">
          <button class="first-row">e</button>
          <button class="first-row">&#181;</button>
          <button class="first-row">sin</button>
        </div>

        <div class="calc-row">
          <button class="backtrack">Ac</button>
          <button class="backtrack" id="freccia"></button>
          <button class="operators">/</button>
        </div>

        <div class="calc-row">
          <button class="numbers">7</button>
          <button class="numbers">8</button>
          <button class="numbers">9</button>
        </div>

        <div class="calc-row">
          <button class="numbers">4</button>
          <button class="numbers">5</button>
          <button class="numbers">6</button>
        </div>

        <div class="calc-row">
          <button class="numbers">1</button>
          <button class="numbers">2</button>
          <button class="numbers">3</button>
        </div>

        <div class="calc-row">
          <button class="numbers" id="zero">0</button>
          <button class="numbers">.</button>
        </div>
      </div>

      <div class="right-box">
        <button class="first-row">deg</button>
        <button class="operators">*</button>
        <button class="operators">-</button>
        <button id="plus">+</button>
        <button id="equal">=</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  margin: 5vh;
  background-color: black;
  height: 85vh;
  width: 20vw;
  padding: 30px;
  display: flex;
  flex-direction: column;
}
.lower-box {
  display: flex;
  flex-direction: row;
  width: 100%;
}
.right-box {
  display: flex;
  flex-direction: column;
  width: 100%;
}
.left-box {
  width: 100%;
}
#schermo {
  width: 100%;
  height: 30%;
  color: white;
  font-size: 40px;
  text-align: right;
  padding: 20px;
  margin-top: 20%;
}
.calc-row {
  display: flex;
  flex-direction: row;
  margin-bottom: 3%;
}
.first-row {
  width: 22%;
  height: 40px;
  font-size: 20px;
  padding: 5px;
  border-radius: 38%;
}
.first-row:nth-of-type(2) {
  margin: 0 4% 0 4%;
}
.first-row:nth-of-type(3) {
  margin: 0 4% 0 0;
}
.backtrack {
  width: 22%;
  height: 60px;
  font-size: 25px;
  padding: 5px;
  border-radius: 25%;
  background-color: #909497;
}
.backtrack:nth-of-type(2) {
  margin: 0 4% 0 4%;
}
.operators {
  width: 22%;
  height: 60px;
  font-weight: 500;
  font-size: 40px;
  padding: 5px;
  border-radius: 25%;
  background-color: #0080ff;
  color: #5ea8f3;
}
.operators:nth-of-type(3) {
  margin: 0 4% 0 0;
}
#freccia {
  background-image: url(img/backspace.svg);
  background-repeat: no-repeat;
  background-size: 35%;
  background-position: center;
}
.numbers {
  width: 22%;
  height: 60px;
  font-weight: 500;
  font-size: 40px;
  padding: 5px;
  border-radius: 25%;
}
#plus {
  width: 22%;
  height: 100px;
  font-weight: 500;
  font-size: 40px;
  padding: 5px;
  border-radius: 25%;
  background-color: #0080ff;
  color: #5ea8f3;
}
#equal {
  width: 22%;
  height: 100px;
  font-weight: 500;
  font-size: 40px;
  padding: 5px;
  border-radius: 25%;
  background-color: #0080ff;
  color: #5ea8f3;
}
</style>
