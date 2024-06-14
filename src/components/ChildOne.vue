<template>
    <div class="child-one">
      <button @click="sendDataToParent">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChildOne',
    methods: {
      sendDataToParent() {
        this.$emit('sendData', 'Hello from ChildOne!');
      }
    }
  };
  </script>
  
  <style scoped>
  .child-one {
    margin-bottom: 20px;
  }
  
  button {
    background-color: #42b983;
    color: white;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #358a6b;
  }
  </style>
  