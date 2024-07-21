<script setup lang="ts">
import { ref } from "vue";
const risultato_schermo = ref("");
const risultato_reale = ref(0);

function nuovo_input(input: number | string) {
  risultato_schermo.value += input;
}

function clear() {
  risultato_schermo.value = "";
}

function clear_last() {
  risultato_schermo.value = risultato_schermo.value.substring(
    0,
    risultato_schermo.value.length - 1
  );
}

function elaborate_result() {
  try {
    eval(risultato_schermo.value);
  } catch (e) {
    if (e instanceof SyntaxError) {
      alert("Sintassi sbagliata!");
    }
  }

  risultato_reale.value = eval(risultato_schermo.value);
  alert(risultato_reale.value);
  risultato_schermo.value = "";
}
</script>

<template>
  <div class="global">
    <div class="calc">
      <div class="upper-box">
        <div class="result">{{ risultato_schermo }}</div>
      </div>
      <div class="lower-box">
        <div class="calc-row">
          <div class="grey-op" @click="clear_last()">AC</div>
          <div class="grey-op" @click="clear()">C</div>
          <div class="grey-op" @click="nuovo_input('%')">%</div>
          <div class="orange-op" @click="nuovo_input('/')">/</div>
        </div>
        <div class="calc-row">
          <div class="numbers" @click="nuovo_input(7)">7</div>
          <div class="numbers" @click="nuovo_input(8)">8</div>
          <div class="numbers" @click="nuovo_input(9)">9</div>
          <div class="orange-op" @click="nuovo_input('*')">*</div>
        </div>
        <div class="calc-row">
          <div class="numbers" @click="nuovo_input(4)">4</div>
          <div class="numbers" @click="nuovo_input(5)">5</div>
          <div class="numbers" @click="nuovo_input(6)">6</div>
          <div class="orange-op" @click="nuovo_input('-')">-</div>
        </div>
        <div class="calc-row">
          <div class="numbers" @click="nuovo_input(1)">1</div>
          <div class="numbers" @click="nuovo_input(2)">2</div>
          <div class="numbers" @click="nuovo_input(3)">3</div>
          <div class="orange-op" @click="nuovo_input('+')">+</div>
        </div>
        <div class="calc-row">
          <div class="numbers" id="zero" @click="nuovo_input(0)">0</div>
          <div class="numbers" @click="nuovo_input(',')">,</div>
          <div class="orange-op" @click="elaborate_result()">=</div>
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
