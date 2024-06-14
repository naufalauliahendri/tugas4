<template>
  <div id="app">
    <h1>Nested Components with Event Emitting and Slots</h1>
    <ChildOne @sendData="displayData" />
    <ChildTwo>
      <template v-slot:default>
        <p>This is content from Parent Component inserted via slot.</p>
      </template>
    </ChildTwo>
    <ChildThree :parentData="parentData" />
    <p v-if="parentData">Data from ChildOne: {{ parentData }}</p>
  </div>
</template>

<script>
import ChildOne from './components/ChildOne.vue';
import ChildTwo from './components/ChildTwo.vue';
import ChildThree from './components/ChildThree.vue';

export default {
  name: 'App',
  components: {
    ChildOne,
    ChildTwo,
    ChildThree
  },
  data() {
    return {
      parentData: ''
    };
  },
  methods: {
    displayData(data) {
      this.parentData = data;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  color: #42b983;
}
</style>
