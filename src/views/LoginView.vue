<template>  
  <HeadComponent/>
  <div class='authorization'>
    <p style='text-align: center; font-size: 4vh; font-weight: 600;'>Вход</p>
    <div class='authorizationArea'>
      
      <div class="input-with-placeholder">
        <input type='email' id='email' placeholder='' />
        <label class='noselect' for='email'>Введите почту</label>
      </div>
      <div class="input-with-placeholder">
        <input type='password' id='password' placeholder='' />
        <label class='noselect' for='password'>Введите пароль</label>
        <img v-if="hiddenPass" @click="hidePassword()" class='showPassword' src='../assets/eye.svg'/>
        <img v-else @click="hidePassword()" class='showPassword' src='../assets/eye-off.svg'/>
      </div>
      <div class='loginButton'>
        ВОЙТИ
      </div>
      <p>Нет аккаунта? <a href='/register' style='text-decoration: none; color: #f68221'>Зарегистрироваться</a></p>
    </div>
  </div>
</template>

<script>
import HeadComponent from '../components/header.vue'
export default {
  name: 'LoginView',
  components: {
    HeadComponent
  },
  data() {
    return {
      hiddenPass: true
    }
  },
  methods: {
    hidePassword() {
      this.hiddenPass = !this.hiddenPass
      if (this.hiddenPass == true) {
        document.getElementById('password').type = 'password'
      }
      else {
        document.getElementById('password').type = 'text'
      }
    }
  }
}
</script>
<style scoped>
.authorization {
  display: block;
  margin: 0 auto;
  width:60vw;
  height: 50vh;
}
.authorizationArea {
  width:50%;
  margin: 0 auto;
  /* border: 2px solid #f68221; */
  height: 100%;
  text-align: center;
  position: relative;
}
.input-with-placeholder {
  width: 70%;
  position: relative;
  margin: 0 auto;
  cursor:text;
  margin-top: 25px;
}
.input-with-placeholder label {
  position: absolute;
  top: 0;
  left: 0;
  width: 70%;
  height: 100%;
  display: flex;
  align-items: center;
  padding-left: 4vw;
  transition: 300ms all;
  color: black;
  font-size: 2vh;
  cursor: text;
  font-family: 'Anonymous';
}
* {
  box-sizing:border-box;
}
.input-with-placeholder input {
  width: 100%;
  height: 6vh;
  margin: 0 auto;
  outline: none;
  padding-left: 4vw;
  padding-top:2%;
  border-width: 0px;
  border-radius: 565px;
  background: #fcfcfc;
  box-sizing: border-box;
  font-size: 2vh;
  transition: 0.3s;
  border-color: black;
  border-width: 1px;
  box-sizing:border-box;

}
.input-with-placeholder input:hover {
  border: 1px solid #f68221;
  transition: 0.3s;
}
.input-with-placeholder input:focus {
  border: 1px solid #f68221;
  transition: 0.3s;
}
.input-with-placeholder input:focus~label,
.input-with-placeholder input:not(:placeholder-shown)~label {
  height: 50%;
  padding-left: 4vw;
  transform: translateY(-0.4vh);
  font-size: 1.1vh;
  color: #777;
}
.showPassword {
  width: 7%;
  position: absolute;
  right: 5%;
  top: 25%;
  cursor: pointer;
}
.loginButton {
  background-color:#f68221;
  width: 70%;
  height: 12%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto;
  border-radius: 575px;
  color: white;
  letter-spacing: 3px;
  font-family: 'Open Sans';
  font-size: 2vh;
  margin-top: 5%;
  transition: 0.5s;
  cursor: pointer;
}
.loginButton:hover {
  filter: drop-shadow(0px 0px 7px #f68221);
  transition: 0.5s;
}
#email {
  background-image: url(../assets/email.svg);
  background-repeat: no-repeat;
  background-position: 6% 50%;
  background-size: 7%;
}
#password {
  background-image: url(../assets/password.svg);
  background-repeat: no-repeat;
  background-position: 6% 50%;
  background-size: 6%;
}

.noselect {
  -webkit-touch-callout: none; /* iOS Safari */
    -webkit-user-select: none; /* Safari */
     -khtml-user-select: none; /* Konqueror HTML */
       -moz-user-select: none; /* Old versions of Firefox */
        -ms-user-select: none; /* Internet Explorer/Edge */
            user-select: none; /* Non-prefixed version, currently
                                  supported by Chrome, Edge, Opera and Firefox */
}
</style>
