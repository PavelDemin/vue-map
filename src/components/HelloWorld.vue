<template>
  <div>
    <button @click='hide=!hide'>Кнопка</button>
    <transition>
      <div v-if='hide'>Жопа появилась!</div>
    </transition>
    <h1>{{ title }}</h1>
    <diV>Текущая дата: {{ date }}</diV>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    title: String,
    date: Date 
    
  },
  data: function () {
    return {
      hide: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
