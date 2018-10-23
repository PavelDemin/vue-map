<template>
   <div id="app" class="nul">
    <div>{{msg}}</div>
    <HelloWorld title='Заголовок блеать!' v-bind:date=datet></HelloWorld>
   </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  methods:{
    datet: function() {
      let d = new Date()
      return d.getDate()
    }
  },
  data() {
    return {
      msg: 'Добро пожаловать!'
    }
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
