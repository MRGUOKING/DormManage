<template>
  <div>
    <article class="background">
    </article>
<!--    登录的主题内容-->
    <article class="login-container">
<!--      登录文字-->
      <section class="login-title">
        后台管理
      </section>

      <section class="login-item">
        <p class="text">用户名</p>
        <input type="text">
      </section>
      <section class="login-item">
        <p class="text">密码</p>
        <input type="password">
      </section>
<!--      登录按钮-->
      <section>
        <button class="login-submit" @click="login">登录</button>
      </section>
    </article>
  </div>
</template>

<script>
export default {
  name: "Login",
  methods:{
    login(){
      this.$router.replace('/article')
    }
  },
  mounted() {
    document.querySelector("body").className += 'background'
  }
}
</script>

<style scoped>
.background{
  background: url("./images/bgc3.jpg") no-repeat fixed;
  filter: blur(5px) brightness(90%) saturate(150%);
  background-size: 100% 100%;
  position: fixed;
  height: 100%;
  width: 100%;
  z-index: -1;
}
.login-container{
  width: 25%;
  height: 60%;
  z-index: 100;
  position: fixed;
  margin: auto;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  background-color: rgba(255,255,255,0.2);
  border-radius: 5px;
  padding: 10px 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.login-container .login-item{
  width: 90%;
  height: 40px;
  /*background-color: pink;*/
  margin: 20px 0;
  display: flex;
  justify-content: space-between;
  border-bottom: 1.5px solid rgb(200,200,200);
}

.login-item .text{
  width: 20%;
  /*background-color: pink;*/
  font-size: 18px;
  color: rgb(180,180,180);
  text-align: right;
  line-height: 40px;
  margin-right: 10px;
}

.login-container section input{
  width: 100%;
  outline: none;
  background-color: rgba(255,255,255,0);
  font-family: 'SimHei';
  /*background-color: pink;*/
  font-size: 30px;
  color: white;

}
/*.login-container section input::-webkit-input-placeholder {*/
/*  color: rgb(180,180,180);*/
/*  font-size: 20px;*/
/*  font-weight: 5;*/
/*  margin-top: 3px;*/
/*  position: relative;*/
/*  top: 5px;*/
/*  left: 5px;*/
/*}*/

.login-container .login-title{
  border: none;
  margin: 0 auto;
  margin-bottom: 60px;
  font-size: 50px;
  color: white;
  text-align: center;
}

.login-submit{
  width: 200px;
  height: 40px;
  border-radius: 5px;
  outline: none;
  border: none;
  font-size: 25px;
  font-weight: 1000;
  color: white;
  background:linear-gradient(to bottom right, #a3bcb1,#37b9e9);/*设置按钮为渐变颜色*/
  transition: all 0.2s;
  cursor: pointer;
}

.login-submit:hover{
  background:linear-gradient(to bottom right,#37b9e9, #a3bcb1);
  color: purple;
}
</style>
