<template>
  <a-layout id="components-layout-demo-custom-trigger">
    <a-layout-sider
      :trigger="null"
      collapsible
      v-model="collapsed"
    >
      <div class="logo"></div>
      <a-menu theme="dark" mode="inline" :defaultSelectedKeys="['1']">
        <a-sub-menu key="sub1">
          <span slot="title"><a-icon type="mail" /><span>我的竞价项目</span></span>
          <a-menu-item key="1"><router-link to="/home/my-project">我的项目</router-link></a-menu-item>
          <a-menu-item key="2"><router-link to="/home/my-project">已委托项目</router-link></a-menu-item>
          <a-menu-item key="3"><router-link to="/home/my-project">编制完成项目</router-link></a-menu-item>
          <a-menu-item key="4"><router-link to="/home/my-project">通过审核项目</router-link></a-menu-item>
          <a-menu-item key="5"><router-link to="/home/my-project">已公布项目</router-link></a-menu-item>
          <a-menu-item key="6"><router-link to="/home/my-project">正在报名</router-link></a-menu-item>
          <a-menu-item key="7"><router-link to="/home/my-project">正在报价</router-link></a-menu-item>
          <a-menu-item key="8"><router-link to="/home/my-project">报价完毕等待审批</router-link></a-menu-item>
          <a-menu-item key="9"><router-link to="/home/my-project">待确认结果</router-link></a-menu-item>
          <a-menu-item key="10"><router-link to="/home/my-project">终止项目</router-link></a-menu-item>
          <a-menu-item key="11"><router-link to="/home/my-project">废标项目</router-link></a-menu-item>
          <a-menu-item key="12"><router-link to="/home/my-project">结项项目</router-link></a-menu-item>
        </a-sub-menu>
        <a-sub-menu key="sub2">
          <span slot="title"><a-icon type="mail" /><span>我的调研项目</span></span>
          <a-menu-item key="o5">Option 5</a-menu-item>
          <a-menu-item key="o6">Option 6</a-menu-item>
          <a-menu-item key="o7">Option 7</a-menu-item>
          <a-menu-item key="o8">Option 8</a-menu-item>
        </a-sub-menu>
        <a-menu-item key="1">
          <a-icon type="folder"/>
          <span>我的代理机构</span>
        </a-menu-item>
        <a-sub-menu key="sub3">
          <span slot="title"><a-icon type="mail" /><span>我的验收项目</span></span>
          <a-menu-item key="5">Option 5</a-menu-item>
          <a-menu-item key="6">Option 6</a-menu-item>
          <a-menu-item key="7">Option 7</a-menu-item>
          <a-menu-item key="8">Option 8</a-menu-item>
        </a-sub-menu>
         <a-menu-item key="2">
          <a-icon type="video-camera"/>
          <span>新用户管理</span>
        </a-menu-item>
      </a-menu>
    </a-layout-sider>
    <a-layout>
      <a-layout-header style="background: #fff; padding: 0">
        <a-icon
          class="trigger"
          :type="collapsed ? 'menu-unfold' : 'menu-fold'"
          @click="()=> collapsed = !collapsed"
        />
      </a-layout-header>
      <a-layout-content :style="{ margin: '24px 16px', padding: '24px', background: '#fff', minHeight: '280px' }">
        <router-view></router-view>
      </a-layout-content>
    </a-layout>
  </a-layout>
</template>
<script>
  export default {
    data () {
      return {
        collapsed: false
      }
    },
    comments: {
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
