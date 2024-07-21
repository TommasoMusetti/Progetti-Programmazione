<script setup lang="ts"></script>

<template>
  <div class="global">
    <div class="calc">
      <div class="upper-box">
        <div class="result">0</div>
      </div>
      <div class="lower-box">
        <div class="calc-row">
          <div class="grey-op">AC</div>
          <div class="grey-op">C</div>
          <div class="grey-op">%</div>
          <div class="orange-op">/</div>
        </div>
        <div class="calc-row">
          <div class="numbers">7</div>
          <div class="numbers">8</div>
          <div class="numbers">9</div>
          <div class="orange-op">x</div>
        </div>
        <div class="calc-row">
          <div class="numbers">4</div>
          <div class="numbers">5</div>
          <div class="numbers">6</div>
          <div class="orange-op">-</div>
        </div>
        <div class="calc-row">
          <div class="numbers">1</div>
          <div class="numbers">2</div>
          <div class="numbers">3</div>
          <div class="orange-op">+</div>
        </div>
        <div class="calc-row">
          <div class="numbers" id="zero">0</div>
          <div class="numbers">,</div>
          <div class="orange-op">=</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.global {
  background-color: grey;
  background-image: radial-gradient(white 20%, black);
  height: 100vh;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: Arial;
}
.calc {
  background-color: black;
  height: 800px;
  width: 350px;
  display: flex;
  flex-direction: column;
  padding: 20px;
  border-radius: 50px;
}
.upper-box {
  height: 30%;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: flex-end;
}
.result {
  font-size: 50px;
  color: white;
  margin: 20px;
}
.lower-box {
  height: 70%;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 30px;
}
.calc-row {
  display: flex;
  justify-content: space-around;
  gap: 10px;
}
.grey-op {
  background-color: rgb(177, 174, 174);
  display: flex;
  justify-content: center;
  align-items: center;
  width: 70px;
  height: 70px;
  border-radius: 50px;
  padding: 5px;
  font-size: 35px;
  font-weight: 500;
}
.numbers {
  background-color: rgb(71, 69, 69);
  display: flex;
  justify-content: center;
  align-items: center;
  width: 70px;
  height: 70px;
  border-radius: 50px;
  padding: 5px;
  font-size: 40px;
  font-weight: 500;
  color: white;
}
#zero {
  width: 160px;
}
.orange-op {
  background-color: rgb(255, 153, 0);
  display: flex;
  justify-content: center;
  align-items: center;
  width: 70px;
  height: 70px;
  border-radius: 50px;
  padding: 5px;
  font-size: 45px;
  font-weight: 500;
  color: white;
}
</style>
