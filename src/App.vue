<template>
  <div>
  <!-- Navigation -->
  <at-menu mode="horizontal" active-name="1">
    <at-menu-item name="1"><i class="icon icon-home"></i>Navigation One</at-menu-item>
    <at-menu-item name="2"><i class="icon icon-layers"></i>Navigation Two</at-menu-item>
    <at-submenu>
      <template slot="title"><i class="icon icon-life-buoy"></i>Navigation Three</template>
      <at-menu-item name="3-1"><i class="icon icon-settings"></i>Submenu One</at-menu-item>
      <at-menu-item name="3-2"><i class="icon icon-settings"></i>Submenu Two</at-menu-item>
      <at-submenu>
        <template slot="title"><i class="icon icon-life-buoy"></i>Submenu Three</template>
        <at-menu-item name="3-3-1"><i class="icon icon-settings"></i>Submenu Four</at-menu-item>
        <at-menu-item name="3-3-2"><i class="icon icon-settings"></i>Submenu Five</at-menu-item>
      </at-submenu>
    </at-submenu>
    <at-menu-item name="4"><i class="icon icon-settings"></i>Navigation Four</at-menu-item>
  </at-menu>
  <!-- #/Navigation -->
  <div id="app">
    <!-- Cards -->
    <div class="row at-row no-gutter flex-around">
      <div v-for="n in 3" :class="`col-md-7`">
        <at-card :style="{ width: '300px' }">
          <h4 slot="title">Card Title {{n}}</h4>
          <div slot="extra"><a>Extra</a></div>
          <div>
            Card Content
          </div>
        </at-card>
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

export default {
  name: 'App',
  components: {
    Table,
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
