<template>
  <div class="header-top">
     <Row>
        <Col span="8">
          <span>{{welcome}}</span>
          <span> 
            [
              <i-button type="error" size="small">登录</i-button>
              <i-button type="primary" size="small">注册</i-button>
            ]
          </span>
          <span>
            <DropMenu :txt="menu_1.txt" :list="menu_1.list"></DropMenu>
          </span>
        </Col>
        <Col span="8" offset="8">
          <span>{{weixin}}</span>
          <span>{{app}}</span>
          <span>
            <DropMenu :txt="menu_2.txt" :list="menu_2.list"></DropMenu>
          </span>
          <span>
            <DropMenu :txt="menu_3.txt" :list="menu_3.list"></DropMenu>
          </span>
          <span>English</span>
        </Col>
    </Row>
  </div>
</template>

<script>
import DropMenu from './../dropdownMenu'
export default {
  name: 'HeaderTop',
  data () {
    return {
      welcome:'欢迎来到大觅网',
      weixin:'大觅网微信',
      app:'手机版',
      menu_1:{
        txt:'我的大觅',
        list:['驴打滚','炸酱面','豆汁儿']
        },
      menu_2:{
        txt:'客户服务',
        list:['驴打滚','炸酱面','豆汁儿']
        },       
      menu_3:{
        txt:'网站导航',
        list:['驴打滚','炸酱面','豆汁儿']
        },     
    }
  },
  components:{
    DropMenu
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header-top {
  padding:3px 30px;
  background-color:#f5f5f5;
}
.header-top span{
  margin:0 5px;
}
</style>