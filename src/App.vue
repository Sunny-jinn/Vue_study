<template>
  <div>
    <a>Hello</a>
    <h2 @click="num_incre += 1">{{num_incre}}</h2>
  </div>
  <div>
    <a>{{인사}}</a>
  </div>
</template>

<script>

export default {
  data() {
    return {
      num_incre : 0,
      인사 : "Hello",
      num : [1,2,3,4]
    }
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
