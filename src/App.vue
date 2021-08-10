<template>
  <div class="banner" v-if="chk==false">
    <a @click="sub_name='Kim'" :class="{salmon : sub_name == 'Kim'}">김영진</a>
    <a @click="sub_name='Babo'" :class="{salmon : sub_name == 'Babo'}">이현빈</a>
    <a @click="sub_name='Ilbe'" :class="{salmon : sub_name == 'Ilbe'}">이병진</a>
    <a @click="sub_name='Choi'" :class="{salmon : sub_name == 'Choi'}">최수완</a>
    <a @click="sub_name='Yoon'" :class="{salmon : sub_name == 'Yoon'}">윤상필</a>
  </div>
  
  <button @click="chk = !chk" class="btn1"> 전환</button>
  
  <div v-if="chk == false">
    <br /> <br />
    <img src="./assets/Kim.png" v-if="sub_name == 'Kim' ">
    <img src="./assets/Babo.png" v-if="sub_name == 'Babo'">
    <img src="./assets/Ilbe.png" v-if="sub_name == 'Ilbe'">
    <img src="./assets/Choi.png" v-if="sub_name == 'Choi'">
    <img src="./assets/Yoon.png" v-if="sub_name == 'Yoon'">
  </div>
  <div class ="banner2" v-if="chk == true">
    <a v-bind:href="link">hello</a>
  </div>
</template>

<script>

export default {
  data() {
    return {
      chk : false,
      sub_name : "",
      link : "https://fow.kr",

    }
    
  }
}
</script>

<style>

img {
  width: 500px; height: 500px;
}


body {
  margin: 0px;
}

div {
  box-sizing: border-box;
}

.banner {
  padding: 12px;
  border-radius: 10px;
  background:yellowgreen;
  
}

.banner a {
  color: white;
  font-size: 20px;
  font-weight: bold;
  padding: 10px;
}

.banner2 {
  padding: 12px;
  background: violet;
  border-radius: 10px;
}

.banner2 a {
  color: white;
  font-size: 20px;
  font-weight: bold;
  padding: 10px;
}
.salmon {
  color: lightcoral !important;
  text-shadow: 1px 1px 1px lightgrey;
}

.banner a:hover {
  color: lightcoral;
}

.btn1 {
  background: white;
  border: 0px;
  border-radius: 20px;
  padding : 3px;
  float: right;
  position: fixed;
  right: 12px;
  /* bottom: 40px; */
  top: 14px;
  box-shadow: 1px 1px 1px lightslategray;
  transition-duration: 0.3s;
}

.btn1:hover {
  background: lightgrey;
}

.btn1:active {
  margin-left:1px;
  margin-top:1px;
  box-shadow: none;
}



#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
