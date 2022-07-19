<template>
  <div class="header">
   <div class="header__toppart">   
     <div class="header__toppart__location">
            <div><img alt="item" src="../assets/i/location.svg"></div><div>Волгоградская область</div></div>
      <div class="header__toppart__upleftmenu">
            <div class="header__toppart__upleftmenu__services"><div>Тендеры</div><div>Базы подрядчиков</div><div>Другие сервисы<img alt="item" src="../assets/i/arrow-down.png"></div></div>
            </div>
     </div>
   
  <div class="header__lowerpart">
    <div class="header__lowerpart__logo"><img alt="item" src="../assets/i/logo.svg"></div>
    <div class="header__lowerpart__catalog"><img alt="item" src="../assets/i/menu-icon.svg">Каталог</div>
    <Search />
    <List />
    <div class="header__lowerpart__login">А
    </div>
  </div>
  </div>

</template>
<script>
import Search from "@/components/Search"
import List from "@/components/List"

export default {
  components: {
    Search,
    List
  }
}
</script>
  /*header style*/
<style>
.header__toppart { 
  display: flex;
  justify-content: space-between;
  justify-items: center;
  height: 32px;
  margin: 0 6%; 
  font-size: 12px;
}
.header__toppart__location div{
  padding: .2em;
}
.header__toppart__upleftmenu{
  display: flex;
  align-items: center;
  justify-content: center;
}
.header__toppart__location{
  display: flex;
  justify-content: space-around;
  justify-items: center;
}
.header__toppart__upleftmenu__services div{
  padding: .9em;
}
.header__toppart__upleftmenu__services{
  display: flex;
  justify-content: space-around;
}
.header__lowerpart__login{
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #9B51E0;
  color: white;
  vertical-align: middle;
  line-height: 50px;
}
.header__lowerpart {
  display: flex;
  justify-content: space-around;
  padding: .6em 0;
  height: 76px;
}
.header__lowerpart__catalog{
  background-color: #FED83D;
  border-radius: 4px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 .7em;
  font-weight: 600;
}
.header__lowerpart__catalog img{ 
  padding-right: .2em;
}



</style>