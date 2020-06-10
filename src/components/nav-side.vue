<template>

  <div class="nav-side" v-show="sideState">
    <div class="logo">
      <img src="@/assets/img/logo_b.png">
    </div>
    <div class="menu">
      <v-btn text href="#home" @click="sideOpen(false)">Home</v-btn>
      <v-btn text href="#intro" @click="sideOpen(false)">데일리세탁</v-btn>
      <v-btn text href="#how" @click="sideOpen(false)">이용방법</v-btn>
      <v-btn text href="#faq" @click="sideOpen(false)">자주묻는 질문</v-btn>
      <v-btn text href="#customer" @click="sideOpen(false)">고객센터</v-btn>
    </div>
    <v-btn class="close" text @click="sideOpen(false)">
      <v-icon>mdi-close</v-icon>
    </v-btn>
  </div>

</template>

<script>
export default {
  data() {
    return {
      sideState:false,
    }
  },
  methods: {
    sideOpen(item){
      this.sideState = item
    }
  },
}
</script>

<style lang="scss" scoped>

.nav-side{
  font-family:'SCDream';
  position:fixed;
  width:240px;
  height:100%;
  right:0px;
  background: #fff;
  z-index:3;
  border-left:1px solid #e2e2e2;

  .logo{
    border-bottom:1px solid #e2e2e2;
    padding:30px 50px;
    img{width:100%;}
  }

  .menu{
    display:flex;
    flex-direction: column;
    margin-top:20px;

    .v-btn{
      border-radius:0px;
      justify-content: flex-start;
      height:50px;
      font-weight:400;
    }
  }

  .v-btn.close{
    position:absolute;
    top:0px;
    right:0px;
    min-width:50px;
    height:50px;
    border-radius:50%;
    padding:0px;
    
  }
}

@media screen and(min-width:1200px){
  .nav-side{display:none;}
}

</style>