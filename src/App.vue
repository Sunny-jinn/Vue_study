<template>
  <div class="banner" v-if="chk==false">
    <a @click="sub_name='Kim'" :class="{salmon : sub_name == 'Kim'}">김영진</a>
    <a @click="sub_name='Babo'" :class="{salmon : sub_name == 'Babo'}">이현빈</a>
    <a @click="sub_name='Ilbe'" :class="{salmon : sub_name == 'Ilbe'}">이병진</a>
    <a @click="sub_name='Choi'" :class="{salmon : sub_name == 'Choi'}">최수완</a>
    <a @click="sub_name='Yoon'" :class="{salmon : sub_name == 'Yoon'}">윤상필</a>
    <button @click="chk = !chk, sub_name = ''" class="btn1"> 전적검색</button>

  </div>
  
  
  <div v-if="chk == false">
    <br /> <br />
    <img src="./assets/Kim.png" v-if="sub_name == 'Kim' ">
    <img src="./assets/Babo.png" v-if="sub_name == 'Babo'">
    <img src="./assets/Ilbe.png" v-if="sub_name == 'Ilbe'">
    <img src="./assets/Choi.png" v-if="sub_name == 'Choi'">
    <img src="./assets/Yoon.png" v-if="sub_name == 'Yoon'">
  </div>
  <div class ="banner2" v-if="chk == true">
    <a style=text-decoration:none; v-bind:href="link_fow + this.nick">FOW</a>
    <a style=text-decoration:none; v-bind:href="link_opgg + this.nick">OP.GG</a>
    <a>하이</a>
    
  </div>
  <div class ="" v-if="chk == true">
    <br /><br/>
    <a class="name">닉네임을 입력하세요.<br/></a>
    <form v-on:submit="onSubmit">
      <input type = "text" v-model="nick" class = "inpt1" placeholder="ex) 비누효과">
    </form>
    <button @click="chk = !chk, sub_name = ''" class="btn1">얼굴</button>

  </div>
</template>

<script>

export default {
  data() {
    return {
      chk : false,
      sub_name : "",
      link_fow : "https://fow.kr/find/",
      link_opgg : "https://op.gg/summoner/userName=",
      nick : "",

    }
  },
  methods: {
    onSubmit(e) {
      e.preventDefault();
    }
  },
}
</script>

<style>

img {
  position: relative;
  width: 800px; height: 700px;
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
  /* text-shadow: 1px 1px 1px rgb(240, 219, 219); */
}

.banner a:hover {
  color: lightcoral;
}

.btn1 {
  background: white;
  border: 0px;
  border-radius: 5px;
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

.inpt1 {
  border-radius: 3px;
  padding: 10px;
  font-size:20px;
  border: 1px solid red;
}

.name {
  position: relative;
  font-size: 17px;
  right:50px;
  bottom: 5px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
