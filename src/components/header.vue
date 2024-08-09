<template>
	<header>
    <a href='/'>
      <div class='logo'>
        <img src='../assets/Logo_mini_codologia.png'>
      </div>
    </a>
    
    <div class='menu'>
      <ul>
        <li><a href='/'>Главная</a></li>
        <li><a href='#'>Программа</a></li>
        <li><a href='#'>Контакты</a></li>
      </ul>
    </div>
    <div class='login'>
      <a href='/login'>
        <div class='signIn'>
          Войти
        </div>
      </a>
    </div>
  </header>
</template>

<script>

export default {
	name: 'HeadComponent',
	data() {

	}
}
</script>
<style scoped>
header {
  display: flex;
  flex-flow: row nowrap;
  justify-content: flex-start;
  align-items: center;
  max-width: 60vw;
  margin: 0 auto;
  padding: 5px;
}
a {
  color:black;
  font-family: Anonymous;
  text-decoration: none;
  transition: 0.3s;
}
.menu a:after {
  display: block; /*превращаем его в блочный элемент*/
  content: ""; /*контента в данном блоке не будет поэтому в кавычках ничего не ставим*/
  height: 3px; /*задаём высоту линии*/
  width: 0%; /*задаём начальную ширину элемента (линии)*/
  background-color: #f68221; /*цвет фона элемента*/
  transition: width 0.4s ease-in-out; /*данное свойство отвечает за плавное изменение ширины. Здесь можно задать время анимации в секундах (в данном случае задано 0.4 секунды)*/
}
.menu a:hover:after,
.menu a:focus:after {
  width: 100%;
}
.menu a:hover{
  color:#f68221;
} 

.menu {
  flex-grow: 1;
  text-align: center;
  width:100%;
}
.menu ul {
  display: inline-flex;
  flex-flow: row nowrap;
  margin: 0;
  padding: 0;
  list-style: none;
}
.menu li {
  padding: 15px;
  font-size: 18px;
}
.login {
  width: 15vw;
  display: flex;
  align-items:center;
  justify-content: center;
}
.logo {
  width:12vw;
}
.logo img {
  width:12vw;
}
a {
  text-decoration: none;
}
.signIn {
  border: 3px solid #f68221;
  border-radius: 15px;
  padding:10px 15px 10px 15px;
  width:50%;
  transition: 0.3s;
  text-align: center;

  cursor: pointer;
  a {
    color: black;
  }
}
.signIn:hover {
  background-color: #f68221;
  transition: 0.3s;
  text-decoration: none;
  color: white;
}
</style>