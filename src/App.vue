<template>
  <div class="wrapper">
    <Header />
    <nav class="container">
      <router-link to="/about"><div class='text-nav'><p>Каталог</p> <p class='small-text'>4 442 512</p></div></router-link> <p class='bread'>></p>
      <router-link to="/about"><div class='text-nav'><p>Строительные материалы</p> <p class='small-text'>4 442 512 предложения</p></div></router-link> <p class='bread'>></p>
      <router-link to="/about"><div class='text-nav'><p>Сухие строительные смеси</p> <p class='small-text'>2 442 012 предложения</p></div></router-link> <p class='bread'>></p>
      <router-link to="/about"><div class='text-nav'><p>Шпаклевки</p> <p class='small-text'>1 442 512 предложения</p></div></router-link> <p class='bread'>></p>
      <router-link to="/"><div class='text-nav'><p >Шпаклевка</p> <p class='small-text'></p></div></router-link>
    </nav>  
    <router-view/>
  </div>
</template>
<script>
import Header from "@/components/Header"
export default {
  components: {
    Header
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Montserrat:wght@200;300;400;500;600;700;800;900&family=Open+Sans:wght@300;400;500;700;800&display=swap');
body{
  margin: 0;
}
#app {
  font-family: 'Open Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: 14px;
  line-height: 24px;
}
nav {
  text-align: left;
  display: flex;
  flex-direction: row;
  line-height: 1px;
  text-decoration: none;
  a {
    color: #2c3e50;
    text-decoration: none;

    &.router-link-exact-active {
      color: #05B169;
    }
  }
}
.wrapper{
  margin: 0 auto;
}
.vueperslides__track{
  height: 70px;
}
.vueperslide__content-wrapper{
  height: 70px;
}
.vueperslide vueperslide--visible{
  height: 70px;
}
.vueperslide vueperslide--active vueperslide--visible{
  height: 70px;
}
.vueperslides__track-inner{
  height: 70px;
}
.vueperslides__parallax-wrapper{
  height: 70px;
}
.vueperslides__inner{
  height: 70px;
}
.vueperslides{
  height: 70px;
}
.vueperslide__content-wrapper{
  height: 70px !important;
}
.vueperslides__arrow button{
  width: 50%;
}
.vueperslide__content-wrapper{
  padding-left: 2em;
}
.container {
  margin: 0 6%; 
}
.text-nav{
  display: flex;
  flex-direction: column;
  justify-items: center;
}
.bread {
  margin-top: 4px;
  padding: 1.9em;
}
.small-text{
  font-size: 12px;
  line-height: 20px;
  color: #708598;
  line-height: 1px;
}
  /* mobile version */
@media (max-width: 720px) {
  .nav { font-size: 10px;
  line-height: 24px;}
  .carditem{
    flex-direction: column;
  }
  .header{
    display: none;
  }
  nav{
    display: none;
  }
  .carditem__suggest{
    width: 70vw;
    border: none;
  }
  .carditem__image{
    width: 70vw;
     border: none;
  }
}
</style>
