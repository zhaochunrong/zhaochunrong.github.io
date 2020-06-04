<template>
    <Row gutter="8">
        <Col span="3" v-for="item in list">
           
                <ListMenu :title="item.title" :menu="item.menu" :src="item.url"></ListMenu>
           
        </Col>
    </Row>
</template>

<script>
import ListMenu from './../listMenu';
import weixin from './images/weixin.png';
import app from './images/app.png';
export default{
   name:'FooterTop',
   data(){
       return{
          list:[
              {
                  title:'订购方式',
                  menu:['在线订购','电话订购']
              },
              {
                  title:'订购方式',
                  menu:['在线订购','电话订购']
              },
              {
                  title:'订购方式',
                  menu:['在线订购','电话订购']
              },
              {
                  title:'订购方式',
                  url:weixin
              },
              {
                  title:'订购方式',
                  url:app
              },
              {
                  title:'订购方式',
                  menu:['在线订购','电话订购']
              },
              {
                  title:'订购方式',
                  menu:['在线订购','电话订购']
              },
              {
                  title:'订购方式',
                  menu:['在线订购','电话订购']
              }
          ] 
       }
   },
   components:{
       ListMenu
   }
}
</script>

<style scoped>
</style>