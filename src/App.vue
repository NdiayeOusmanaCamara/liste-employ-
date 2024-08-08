<template>
  <div id="app">
    <EmployeeList />
  </div>
</template>

<script>
import EmployeeList from './components/EmployeeList.vue';

export default {
  components: {
    EmployeeList
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
}
</style>
