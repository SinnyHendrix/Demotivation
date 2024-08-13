<template>
    <div>
     
      <button @click="getQuote">Demotivate Me!</button>
      <p v-if="selectedQuote">Random Quote: {{ selectedQuote.quote }}</p>
    </div>
  </template>
  
  <script>
  import { quotes } from './quotes.js';
  
  export default {
    data() {
      return {
        quotes: quotes,
        selectedQuote: null
      };
    },
    methods: {
        getQuote() {
      const randomIndex = Math.floor(Math.random() * this.quotes.length);
      this.selectedQuote = this.quotes[randomIndex];
      }
    }
  };
  </script>