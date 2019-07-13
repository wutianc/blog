<template>
  <div class="">
    <div class="h_header">
      <ul>
        <li v-for="(item, index) in nav" :key="index">{{item}}</li>
      </ul>
    </div>
  </div>   
</template>

<script>
import { nav } from '../../static/home.json'
import Comfun from '@/common/utils.js'

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      age: ''
    }
  },
  created() {
    this.nav = nav
    this.age = new Comfun().jsGetAge('1990-7-9')
    console.log('tag', this.age)
  }
}
</script>

<style lang="less" scoped>
.h_header {
  width: 100%;
  height: 65px;
  border-bottom: 1px solid #cccccc;
  ul {
    height: 65px;
    display: flex;
    flex-direction: row;
    align-items: center;
    li {
      width: 200px;
      height: 100%;
      line-height: 65px;
      text-align: center;
      &:hover {
        background: #cccccc;
        cursor: pointer;
      }
    }
  }
}
</style>

