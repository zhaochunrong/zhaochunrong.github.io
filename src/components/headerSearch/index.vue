<template>
  <div class="header-search">
    <HeaderSign>
      <Col span="4">
        <span>
          <DropMenu :txt="北京站"></DropMenu>
        </span>  
      </Col>
      <Col span="12">
        
      </Col>
   </HeaderSign>
  </div>
</template>

<script>
import HeaderSign from './../headerSign';
import DropMenu from './../dropdownMenu';
export default {
  name: 'HeaderSearch',
  data () {
    return {
   
    }
  },
  components:{
    HeaderSign,
    DropMenu
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.logo{
  width:100%;
  height:60px;
  padding:5px 0;
}
.logo img{
 width:auto;
 height:60px;
}
</style>