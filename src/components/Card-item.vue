<template>
  <div class='title container'><h1>Штукатурка цементная цокольная Knauf Sockelpultz 25 кг</h1><img alt="item" src="../assets/i/share-icon.svg"></div>
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
  <div class="carditem container">
  <div class="carditem__image">
      <div class="carditem__image__vidgets">
              <div class="carditem__image__vidgets__color">
                    <div class="carditem__image__vidgets__color__orange">
                    Хит продаж
                    </div>
                    <div class="carditem__image__vidgets__color__red">
                    Акция
                    </div>
              </div>
              <div class="carditem__image__vidgets__color__spisok" @click="onclick"><img alt="item" src="../assets/i/plus.svg">Добавить</div>
          </div>
      <div><img alt="item" src="../assets/i/good-item.svg"></div>
    </div>
    <div class="carditem__text">
        <table>
              <tr>
                <td><img alt="item" src="../assets/i/list-list-icon.svg"></td><td class='semibold-text'>Коротко о товаре</td>
              </tr>
              <tr>  
                <td></td><td>Вес · <span class="grey-text">25—50 кг</span></td>
              </tr>
              <tr>
                <td></td><td>Основа ·<span class="grey-text">Гипсовая супер штукатурка Knauf S</span></td>
              </tr>
              <tr>
                <td></td><td class="blue-text">Все  характеристики</td>
              </tr>
              <tr>
                <td><img alt="item" src="../assets/i/like-icon.svg"></td><td class='semibold-text'>Пользуется спросом</td>
              </tr>
              <tr>
                <td></td><td class="underline-text">2 274 просмотров</td>
              </tr>
              <tr>
                <td><img alt="item" src="../assets/i/check-icon.svg"></td><td class='semibold-text'>В наличии в Москве на 4 марта 2020</td>
              </tr>
              <tr>
                <td></td><td class="blue-text">140 предложений</td>
              </tr>
        </table>                  
            <img alt="item" src="../assets/i/knauf.svg">
    </div>

    <div class="carditem__suggest">
              <div class='uppercase-text semibold-text'><img alt="item" src="../assets/i/star-icon.svg">Популярное предложение</div>
              <div class="price-block"><div class='price-text'>39 900 </div><div class="margin-text">РУБ/ ШТ</div></div>
              <div class='green-text'>В наличии</div>
              <div class="catalog">Перейти в магазин</div>
              <div class='postavshik-block'><div ><img alt="item" src="../assets/i/security.svg"></div>
              <div>
              <p class='green-text'>Провереннный поставщик</p>
              <p class="semibold-text">ООО ВсеИнструменты.ру</p>
              <p class='green-text'>Дилер</p>
              </div>
              <div><img alt="item" src="../assets/i/allinstruments.svg"></div>
              </div>
    </div>
      </div> 
  <div class="sliderimg container">
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
import 'vue3-simple-typeahead/dist/vue3-simple-typeahead.css' 

export default {
  name: 'my-vue-component',
  components: { VueperSlides, VueperSlide, SimpleTypeahead },
  data: () => ({
    slides: [
      {
        title: 'Где купить',
        content: 'Штукатурка',
        image: 'https://filvp.github.io/i/good1.svg'
      },
      {
        title: 'Описание',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/item.png'
      },
      {
        title: 'Характеристики',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good3.svg'
      },
      {
        title: 'Календарь низких цен',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good1.svg'
      },
      {
        title: 'Динамика цен',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good1.svg'
      },
       {
        title: 'Сравнение',
        content: 'Slide 2 content.',
        image: 'https://filvp.github.io/i/good1.svg'
      },
       {
        title: 'Рекомендации',
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
      this.list.push("+1")
    }
  }
}
</script>
// styles for card
<style scoped  lang="scss">
.carditem{
  display: flex;
  justify-content: space-around; 
  padding-top: 2em;
}
.carditem__image{
  display: flex;
  height: 290px;
  border: 1px solid #ECEFF1;
  border-radius: 4px;
  flex-direction: column;
  padding: 1.3em;
  width: 30%;
}
.carditem__image__vidgets__color{
  display: flex;
  flex-direction: column;
}
.carditem__image__vidgets{
  display: flex;
  justify-content: space-between;
}
.carditem__image__vidgets__color__orange{
  padding: .6em 1.5em;
  margin: .2em;
  background: #F2994A;
  border-radius: 4px;
  font-size: 10px;
  color: white;
  text-transform: uppercase;
  font-weight: bold;
}
.carditem__image__vidgets__color__red{
  padding: .6em 1.5em;
  margin: .2em;
  background-color: #E92F2F;
  border-radius: 4px;
  font-size: 10px;
  color: white;
  text-transform: uppercase;
  font-weight: bold;
}
.carditem__image__vidgets__color__spisok{
  margin-left: 5em;
  color: #1652F0;
  border: 1px solid #ECEFF1;
  border-radius: 4px;
  height: 35px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 12px;
  padding: 0 .7em;
}
.carditem__text{
  text-align: left;
  padding: 1.3em;
}
.carditem__suggest{
  border: 1px solid #ECEFF1;
  border-radius: 4px;
  text-align: left;
  padding: 1.3em;
  border-top: 4px solid #FED83D;
  width: 27%;
  display: flex;
  flex-direction: column;
  div{
    padding: .4em;
  }
}
.price-text{
  display: flex;
  flex-direction: row;
  justify-items: center;
  font-size: 38px;
  font-weight: bold; 
}
.green-text{
  font-size: 10px;
  line-height: 10px;
  color: #05B169;
  text-transform: uppercase;
  font-weight: 600;
}
.semibold-text{
  font-weight: 600;
}
.uppercase-text{
  text-transform: uppercase;
  font-weight:600;
  img{
    padding-right: .5em;
  }
}
.catalog{
  background-color: #FED83D;
  border-radius: 4px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 .7em;
  margin-top: .9em;
  font-weight: 600;
}
.blue-text{
  color: #1652F0;
}
.underline-text {
  text-decoration: underline;
  text-decoration-style: dotted;
}
.grey-text{
  color: #708598;
}
.margin-text{
  margin-top: 1em;
}
.vueperslides__track{
  height: 70px;
}
.postavshik-block{
  display: flex;
  justify-content:first baseline;
  justify-items: center;
  margin-top: .8em;
}
.price-block{
  display: flex;
  flex-direction: row;
  justify-items: last baseline;
}

.slidertext{
  width: 84%;
  margin: 0 auto;
  height: 70px !important;
  position: relative;
}
.sliderimg{
  width: 30%;
  padding-top: 5em;
  padding-left: 6em;
}
h1{
  text-align: left;
}
.title{
  display: flex;
  flex-direction: row;
  img{
    padding-left: .5em;
  }
}
  /* mobile version */
@media (max-width: 720px) {  
  .carditem__suggest{
    width: 70vw;
    border: none;
  }
  .carditem__image{
    width: 70vw;
     border: none;
  }
  h1{
    line-height: 30px;
  }
}
</style>