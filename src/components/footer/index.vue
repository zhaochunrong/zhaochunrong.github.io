<template>
    <div class="footer">
    <FooterTop></FooterTop>
    <FooterBottom></FooterBottom>
    </div>
</template>

<script>
import FooterTop from './../footerTop';
import FooterBottom from './../footerBottom';
export default{
   name:'MyFooter',
   components:{
       FooterTop,
       FooterBottom
   }
}
</script>

<style scoped>
.footer{
     background-color:rgb(230,230,230);
}
</style>