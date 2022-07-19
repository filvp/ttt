<template>
  <div class="header__search">
    <input list="items">
    <datalist id="items">
      <option v-for="item in items" :key="item">{{item}}</option>
    </datalist>
  </div>
</template>
<script>

export default {
  data(){
   return {
     items: ['Шпаклевка', 'Штукатурка', 'Обои', 'Кровля', 'Строительная смесь', 'Стекловата' ]
   }
  },
  components: {
  }
}
</script>
/*header style*/
<style>
.header__search{
  display: flex;
  justify-content: space-around;
  justify-items: center;
  border-radius: 4px;
  border: 1px solid #ECEFF1;
  height: 40px; 
}
input{
  border-color: #ECEFF1;
  border-style: none;
}
</style>
