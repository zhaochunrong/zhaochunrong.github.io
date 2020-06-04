<template>
  <div class="header">
    <Row>
      <Col span="4">
        <div class="logo">
          <img :src="logo"></img> 
        </div>
      </Col>
      <slot></slot>
    </Row>
  </div> 
</template>

<script>
import Logo from './../../assets/logo.png';
export default {
  name: 'HeaderSign',
  data () {
    return {
    logo:Logo
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header{
  padding:10px 80px;
}
.logo{
  width:100%;
  height:40px;
  border-right:2px solid lightgray;
 
}
.logo img{
 width:auto;
 height:40px;
}
</style>