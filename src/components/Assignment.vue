<template>
    <div id="app">
      <p>Current Count: {{ count }}</p>
      <button @click="increment">Increment</button>
      <button @click="decrement">Decrement</button>
      <br>
      <label for="messageInput">Message:</label>
      <input type="text" id="messageInput" v-model="message">
      <p>Message based on Count: {{ message }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'App',
    data() {
      return {
        count: 0,
        message: ''
      };
    },
    methods: {
      increment() {
        this.count++;
        this.updateMessage();
      },
      decrement() {
        this.count--;
        this.updateMessage();
      },
      updateMessage() {
        if (this.count > 0) {
          this.message = 'Count is positive';
        } else if (this.count < 0) {
          this.message = 'Count is negative';
        } else {
          this.message = 'Count is zero';
        }
      }
    }
  };
  </script>
  
  <style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  
  p {
    font-size: 18px;
    margin-bottom: 10px;
  }
  
  button {
    padding: 10px 15px;
    font-size: 16px;
    margin: 5px;
    cursor: pointer;
    background-color: #4CAF50;
    color: #fff;
    border: none;
    border-radius: 4px;
  }
  
  input {
    padding: 8px;
    font-size: 16px;
    margin-bottom: 10px;
  }
  </style>
  
