<template>
    <div class="child-three" v-if="parentData">
      <p>Data received from Parent: {{ parentData }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChildThree',
    props: {
      parentData: {
        type: String,
        required: false
      }
    }
  };
  </script>
  
  <style scoped>
  .child-three {
    border: 2px solid #42b983;
    padding: 20px;
    margin-top: 20px;
  }
  </style>
  