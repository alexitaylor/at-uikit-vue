<template>
  <div>
  <!-- Navigation -->
  <Nav/>
  <!-- #/Navigation -->
  <div id="app" class="container">
    <!-- Cards -->
    <div class="row at-row no-gutter flex-around">
      <div v-for="n in 3" :class="`col-md-7`" :key="`${n}`">
        <Card/>
      </div>
    </div>
    <!-- #/Cards-->
    <!-- Table -->
    <div id="table">
      <Table/>
    </div>
    <!-- #/Table -->
    <!--<router-view/>-->
  </div>
  </div>
</template>

<script>
import Table from './components/Table';
import Nav from './components/Nav';
import Card from './components/Card';

export default {
  name: 'App',
  components: {
    Table,
    Nav,
    Card,
  },
  data() {
    return {
      value: 'TEST',
    };
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
  #table {
    margin-top: 60px;
  }
</style>
