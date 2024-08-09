<template>  
  <HeadComponent/>
  <div class='main'>
    <div class='aboutUs'>
      <div class='textAbout'>
        <p class='firstTextAbout'>Кодология - это международная сеть цифровых пространств для развития технологических навыков школьников</p>
        <p class='secondTextAbout'>Учим детей кодить, создавать сайты, игры, мобильные приложения, дизайн и 3D проекты, прокачиваем стартап-мышление и soft skills.</p>
      </div>
      <div class='imageAbout'>
        <img src='../assets/aboutImage.png'>
      </div>
    </div>
  </div>
</template>

<script>
import HeadComponent from '../components/header.vue'
export default {
  name: 'HomeView',
  components: {
    HeadComponent
  }
}
</script>
<style scoped>

.main {
  max-width: 60vw;
  display: flex;
  margin: 0 auto;
}
.aboutUs {
  margin-top:5%;
  width:100%;
  display: flex;
}
.textAbout {
  width: 60%;
  line-height: 1.25;
  letter-spacing: 2px;
}
.imageAbout {
  display: inline-flex;
}
.imageAbout img{
  width: 90%;
}
.firstTextAbout {
  font-family: "Anonymous"; 
  font-weight: 700; 
  font-size: 40px;
  text-decoration: underline;
}
.secondTextAbout {
  font-family: "Open Sans"; 
  font-weight: 400;
}

</style>
