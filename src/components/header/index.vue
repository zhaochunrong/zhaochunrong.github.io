<template>
   <div class="header">
      <HeaderTop></HeaderTop>
      <HeaderSearch></HeaderSearch>
   </div>
</template>

<script>
import HeaderTop from './../headerTop';
import HeaderSearch from './../headerSearch';
export default {
  name: 'MyHeader',
  data () {
    return {
    
    }
  },
  components:{
    HeaderTop,
    HeaderSearch
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header{
	background: #FFFFFF;
}
</style>