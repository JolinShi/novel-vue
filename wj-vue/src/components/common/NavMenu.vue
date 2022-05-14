<template>
  <el-menu
    :default-active="'/index'"
    router
    mode="horizontal"
    background-color="white"
    text-color="#222"
    active-text-color="red"
    style="min-width: 1300px">
    <el-menu-item v-for="(item,i) in navList" :key="i" :index="item.name">
      {{ item.navItem }}
    </el-menu-item>
    <span style="position: absolute;padding-top: 20px;right: 60%;font-size: 20px;font-weight: bold">yayanovel</span>
    <el-input
      placeholder="快速搜索..."
      prefix-icon="el-icon-search"
      size="medium"
      style="width: 300px;position:absolute;margin-top: 12px;right: 18%"
      v-model="keywords">
    </el-input>
  </el-menu>

</template>

<script>
export default {
  name: 'NavMenu',
  data () {
    return {
      navList: [
        {name: '/index', navItem: 'Home'},
        {name: '/jotter', navItem: 'Jotter'},
        {name: '/book', navItem: 'Book'},
        {name: '/admin', navItem: '个人中心'}
      ],
      keywords: ''
    }
  }
}
</script>

<style scoped>
  a{
    text-decoration: none;
  }

  span {
    pointer-events: none;
  }
</style>
