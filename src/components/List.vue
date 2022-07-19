<template>
  <div class="list">
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
<style>
.list{
  border: 1px solid grey;
  border-radius: 4px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 .7em;
}
.list img{ 
  padding-right: .2em;
}

</style>