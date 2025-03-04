<template>
    <div>
      <h1>Calculadora</h1>
      <div class="keyboard">
        <button v-for="number in numbers" :key="number" @click="handleClick(number)">
          {{ number }}
        </button>
      </div>
      <p>Has clicat el número: {{ clickedNumber }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9],
        clickedNumber: null,
      };
    },
    methods: {
      handleClick(number) {
        this.clickedNumber = number;
      },
    },
  };
  </script>
  
  <style>
  .keyboard {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
  }
  button {
    padding: 10px;
    font-size: 18px;
  }
  </style>