<head>
<script src="https://unpkg.com/vue"></script>
<script src="https://unpkg.com/vueperslides"></script>
<link href="https://unpkg.com/vueperslides/dist/vueperslides.css" rel="stylesheet">
</head>
<template>
<div class='container'>
  <div class='title'><h1>Штукатурка цементная цокольная Knauf Sockelpultz 25 кг</h1><img alt="item" src="../assets/i/share-icon.svg"></div>
  </div>
  <div class="slidertext container">
    <vueper-slides
        class="no-shadow"
        :visible-slides="5"
        slide-multiple
        :gap="3"
        :slide-ratio="1 / 4"
        :dragging-distance="200"
        :bullets="false"
        :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }">
      <vueper-slide v-for="(slide, i) in slides" :key="i" :title="slide.title" />
    </vueper-slides>
  </div>
  <div class="card-item container">

    <div class="card-image">
      <div class="vidgets">
          <div class="vidgets-color">
                <div class="orange-block">
                Хит продаж
                </div>
                <div class="red-block">
                Акция
                </div>
            </div>
          <div class="v-spisok" @click="onclick"><img alt="item" src="../assets/i/plus.png">Добавить</div>
      </div>
      <div><img alt="item" src="../assets/i/good-item.svg"></div>
    </div>


    <div class="card-text">
    <table>
          <tr>
            <td><img alt="item" src="../assets/i/list-list-icon.svg"></td><td>Коротко о товаре</td>
          </tr>
          <tr>
            <td></td><td>Вес · 25—50 кг</td>
          </tr>
          <tr>
            <td></td><td>Основа. Гипсовая супер штукатурка Knauf S</td>
          </tr>
          <tr>
            <td></td><td class="blue-text">Все  характеристики</td>
          </tr>
          <tr>
            <td><img alt="item" src="../assets/i/like-icon.svg"></td><td>Пользуется спросом</td>
          </tr>
          <tr>
            <td></td><td class="underline">2 274 просмотров</td>
          </tr>
          <tr>
            <td></td><td>В наличии в Москве на 4 марта 2020</td>
          </tr>
          <tr>
            <td></td><td class="blue-text">140 предложений</td>
          </tr>
    </table>                  
            <img alt="item" src="../assets/i/knauf.svg">
    </div>


    <div class="suggest-item">
            <div><img alt="item" src="../assets/i/star-icon.svg">Популярное предложение</div>
            <div class="price-text"><div class='price'>39 900 </div><div>РУБ/ ШТ</div></div>
            <div class='green-text'>В наличии</div>
            <div class="catalog">Перейти в магазин</div>
            <div class='postavshik'><div ><img alt="item" src="../assets/i/secur.png"></div>
            <div>
            <p class='green-text'>Провереннный поставщик</p>
            <p>ООО ВсеИнструменты.ру</p>
            <p class='green-text'>Дилер</p>
            </div>
            <div><img alt="item" src="../assets/i/allinstruments.svg"></div>
            </div>
    </div>
      </div>


 
  <div class="slidertext2 container">
            <vueper-slides
                class="no-shadow"
                :visible-slides="3"
                slide-multiple
                :gap="3"
                :slide-ratio="1 / 4"
                :dragging-distance="200"


                :bullets="false"
                :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }">
              <vueper-slide v-for="(slide, i) in slides" :key="i" :image="slide.image" />
            </vueper-slides>
  </div>
  



</template>
<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'
import SimpleTypeahead from 'vue3-simple-typeahead'
import 'vue3-simple-typeahead/dist/vue3-simple-typeahead.css' //Optional default CSS

export default {
  name: 'my-vue-component',
  components: { VueperSlides, VueperSlide, SimpleTypeahead },
  data: () => ({
    slides: [
      {
        title: 'Штукатурка',
        content: 'Штукатурка',
        image: 'https://filvp.github.io/i/good1.svg'
      },
      {
        title: 'Обои',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good2.svg'
      },
      {
        title: 'Цемент',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good3.svg'
      },
      {
        title: 'Утеплители',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good1.svg'
      },
      {
        title: 'Стекловата',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good1.svg'
      },
       {
        title: 'Теплоизоляторы',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good1.svg'
      },
       {
        title: 'Стекловата',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good1.svg'
      }
    ]
  }),
  computed: {
    list(){
      return this.$store.state.list
    }
  },
  methods: {
    onclick(){
      console.log(this.list)
      this.list.push("Штукатурка")
    }
  }
}
</script>

<style scoped>

.card-item{
  display: flex;
  justify-content: space-around;
 
  padding-top: 2em;

}

.card-image{
  display: flex;
  width: 350px;
  height: 290px;
  border: 1px solid grey;
  border-radius: 4px;
  flex-direction: column;
  padding: 1.3em;
  width: 30%;
}
.card-text{
  text-align: left;
  padding: 1.3em;
}
.vidgets-color{
  display: flex;
  flex-direction: column;
}
.vidgets{
  display: flex;
  justify-content: space-between;
}
.orange-block{
  padding: .6em;
  margin: .2em;
  background: #F2994A;
  border-radius: 4px;
  font-size: 10px;
  color: white;
  text-transform: uppercase;
  font-weight: bold;
}
.red-block{
  padding: .6em;
  margin: .2em;
  background-color: #E92F2F;
  border-radius: 4px;
  font-size: 10px;
  color: white;
  text-transform: uppercase;
  font-weight: bold;
}
.v-spisok{
  margin-left: 5em;
  color: #1652F0;
  border: 1px solid grey;
  border-radius: 4px;
  height: 35px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 12px;
  padding: 0 .7em;
}
.suggest-item{
  border: 1px solid grey;
  border-radius: 4px;
  text-align: left;
  padding: 1.3em;
  border-top: 4px solid #FED83D;
  width: 27%;
  display: flex;
  flex-direction: column;

}
.suggest-item div{
 padding: .1em;

}
.sliderimg{
  /*width: 50%;*/
  padding-top: 5em;
  padding-left: 15em;
  display: flex;
}
.slidertext{
  width: 84%;
  margin: 0 auto;
  height: 70px !important;
  /*padding-top: -350px;*/
  position: relative;
  /* background-color: #ECEFF1; */
}
.slidertext2{
  width: 30%;
  padding-top: 5em;
  padding-left: 5em;
  /*display: flex;*/
  /*height: 70px !important;*/
}
/*.vueperslides {*/
/*  height: 70px;*/
/*}*/
/*.vueperslide__content-wrapper{*/
/*  height: 70px;*/
/*}*/
/*h1{*/
/*  padding: 1em;*/
/*}*/
h1{
  text-align: left;
}
.price{
  font-size: 38px;
  font-weight: bold;
}
.green-text{
  font-size: 10px;
  line-height: 10px;
  color: #05B169;
  text-transform: uppercase;
}


.blue-text{
  color: #1652F0;
}
.underline {
  text-decoration: underline;
  text-decoration-style: dotted;
  /* border-bottom: 1px red solid;
  width: 150px; */
}
.vueperslides__track{
  height: 70px;
}
.postavshik{
  display: flex;
  justify-content:first baseline;
  justify-items: center;
  margin-top: .8em;
}
.price-text{
  display: flex;
  flex-direction: row;
  justify-items: center;
}
.title{
  display: flex;
  flex-direction: row;
}





</style>