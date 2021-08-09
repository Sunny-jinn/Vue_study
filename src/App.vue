<template>
  <div class="banner">
    <a @click="sub_name='Kim'">김영진</a>
    <a @click="sub_name='Babo'">이현빈</a>
    <a @click="sub_name='Ilbe'">이병진</a>
    <a @click="sub_name='Choi'">최수완</a>
    <a @click="sub_name='Yoon'">윤상필</a>
  </div>
  <div>
    <br /> <br />
    <img src="./assets/Kim.png" v-if="sub_name == 'Kim' ">
    <img src="./assets/Babo.png" v-if="sub_name == 'Babo'">
    <img src="./assets/Ilbe.png" v-if="sub_name == 'Ilbe'">
    <img src="./assets/Choi.png" v-if="sub_name == 'Choi'">
    <img src="./assets/Yoon.png" v-if="sub_name == 'Yoon'">
  </div>

</template>

<script>

export default {
  data() {
    return {
      chk : false,
      sub_name : "",

    }
    
  }
}
</script>

<style>

img {
  width: 500px; height: 500px;
}

.Kim {
  color: red;
}

.Babo {
  color: green;
}
.Ilbe {
  color: skyblue;
}
.Choi {
  color: blueviolet;
}
.Yoon {
  color: pink;
}

body {
  margin: 0px;
}

div {
  box-sizing: border-box;
}

.banner {
  padding: 15px;
  border-radius: 10px;
  background:yellowgreen;
  
}

.banner a {
  color: white;
  font-size: 20px;
  font-weight: bold;
  padding: 10px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
