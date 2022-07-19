<template>
  <div class="header__list">
    {{list.join(", ")}}
    <img alt="item" src="../assets/i/list_up.svg">
    Список
  </div>
</template>
<script>
export default {
  data(){
  },
  computed: {
    list(){
      return this.$store.state.list
    }
  },
  components: {
  }
}
</script>
// header style
<style  lang="scss">
.header__list{
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 .7em;
  border: 1px solid #ECEFF1;
  border-radius: 4px;
  height: 40px; 
  font-weight: 600;
  img {
    padding-right: .2em;
  }
}

</style>

