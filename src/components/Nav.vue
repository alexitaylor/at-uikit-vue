<template>
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
</template>

<script>
export default {
  name: 'Nav',
};
</script>
