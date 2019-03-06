<template>
  <layout></layout>
</template>
<script>
  import Layout from '../components/layout/Layout'
  export default {
    data () {
      return {
        collapsed: false
      }
    },
    components: {
      Layout
    }
  }
</script>
<style>
  #components-layout-demo-custom-trigger .trigger {
    font-size: 18px;
    line-height: 64px;
    padding: 0 24px;
    cursor: pointer;
    transition: color .3s;
  }

  #components-layout-demo-custom-trigger .trigger:hover {
    color: #1890ff;
  }

  #components-layout-demo-custom-trigger .logo {
    height: 32px;
    background: rgba(255, 255, 255, .2);
    margin: 16px;
  }
</style>
