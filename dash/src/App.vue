<template>
  <FooterBar class="footer" />
  <div class="container-fluid animate__animated animate__fadeIn">
  </div>
  <router-view />
</template>

<script>
import FooterBar from "@/components/FooterBar.vue";

export default {
  name: 'App',
  components: {
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
  background-color: black;
  transition: all 2s;
}
.container-fluid {
  background-image: url('@/assets/bg.png');
  background-size: cover;
  background-color: black;
  background-repeat: no-repeat;
  background-attachment: fixed;
  width: 100vw;
  height: 100vh;
  position: fixed;
  z-index: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
  z-index: 1;
}
/*Указываю какой шрифт используется в приложении, а так же параметры сглаживания*/
#app {
  font-family: 'Rubik', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f1f1f1;

}

/*Настройки основного контейнера*/
.container {
  width: 100%;
  display: flex;
}
.footer {
  z-index: 999999;
}
</style>