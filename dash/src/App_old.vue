<template>
<!--  <nav>-->
<!--    <router-link to="/">Home</router-link> |-->
<!--    <router-link to="/about">About</router-link>-->
<!--  </nav>-->
<!--  <router-view/>-->
<div class="container animated zoomInUp">
  <ContainerBlock>
  </ContainerBlock>
</div>
  <FooterBar />
</template>

<script>
import FooterBar from "@/components/FooterBar.vue";
import ContainerBlock from "@/components/ContainerBlock.vue";
export default {
  name: 'App',
  components: {
    ContainerBlock,
    FooterBar
  }
}
</script>

<style>
/*Ипортирую шрифт Rubik во всех начертаниях*/
@import url('https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

/*Переменные с цветами для элементов*/
:root {
  --acrylic-blur-dark: rgba(16 18 27 / 40%); /*Прозрачный фон всех элементов*/
  --border-dark: rgba(113 119 144 / 25%); /*Обводка*/
  --content-bg-dark: rgb(146 151 179 / 13%); /*Второй фон для всех элементов*/
  --inactive-color: rgb(113 119 144 / 78%); /*Цвет неактивных ссылок*/
  --active-color: #faf9fb; /*Цвет активных ссылок*/
}

/*Фон*/
html, body {
  background-image: url("./assets/bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}

/*Указываю какой шрифт используется в приложении, а так же параметры сглаживания*/
#app {
  font-family: 'Rubik', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f1f1f1;
  margin-top: 60px;
}

/*Настройки основного контейнера*/
.container {
  width: 100%;
  display: flex;
}

/*Анимация зума*/
@-webkit-keyframes zoomInUp {
  from {
    opacity: 0;
    -webkit-transform: scale3d(0.1, 0.1, 0.1) translate3d(0, 1000px, 0);
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0, 1000px, 0);
    -webkit-animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }

  60% {
    opacity: 1;
    -webkit-transform: scale3d(0.475, 0.475, 0.475) translate3d(0, -60px, 0);
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0, -60px, 0);
    -webkit-animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}

@keyframes zoomInUp {
  from {
    opacity: 0;
    -webkit-transform: scale3d(0.1, 0.1, 0.1) translate3d(0, 1000px, 0);
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0, 1000px, 0);
    -webkit-animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }

  60% {
    opacity: 1;
    -webkit-transform: scale3d(0.475, 0.475, 0.475) translate3d(0, -60px, 0);
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0, -60px, 0);
    -webkit-animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}

.zoomInUp {
  -webkit-animation-name: zoomInUp;
  animation-name: zoomInUp;
}

.animated {
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
}
</style>