<template>
  <div id="app">
    <button @click="click1">
      showMoment
    </button>
    <span v-if="visible1">{{result1}}</span>

  </div>
</template>

<script>

import moment from 'moment'
export default {
  name: 'app',
  data(){
    return {
      visible1 : false
    }
  },
  computed:{
    result1(){
      return moment().format('YYYY年M月DD日HH时mm分ss秒')
    }
  },
  methods:{
    click1(){
      this.visible1 = true
    }
  },
  components: {

  }
}
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
</style>
