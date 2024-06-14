<template>
    <div class="child-two">
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChildTwo'
  };
  </script>
  
  <style scoped>
  .child-two {
    border: 2px dashed #42b983;
    padding: 20px;
    margin-bottom: 20px;
  }
  </style>
  