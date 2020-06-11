<template>
   <div >
    <MyHeader></MyHeader>
    <!--导航部分  商品分类  轮播图组件-->
    <div class="nav" >
    		<div class="navbar">
    		<Menu mode="horizontal">
    				<MenuItem name="0" to="/">首页</MenuItem>
    				<MenuItem name="1" to="/">戏剧</MenuItem>
    				<MenuItem name="2" to="/">体育</MenuItem>
    				<MenuItem name="3" to="/">亲子</MenuItem>
    				<MenuItem name="4" to="/">舞蹈古典</MenuItem>
    				<MenuItem name="5" to="/">摇滚</MenuItem>
    		</Menu>
    		</div>
    		
    		<div class="goodsList" >
    		<h3>全部商品分类</h3>
    		<ul>
    			<li v-for="(item,index) in goodList" :key="index" @mouseenter="show(index)" @mouseleave="hide(index)">
    				<router-link to="/"> 
    					<img :src="iconList[index]"/>
    					{{item}}
    					<span> > </span>
    				</router-link>
    				
    			</li>
    		</ul>
    		</div>
    	   <div  class="goodsListDetail" v-if="IsShow">
    	   	 {{Info}}
    	   </div>
    	   <div class="carousel">
    	   	<Banner></Banner>
    	   </div>
    </div>
    <!-- 展示信息列表-->
    <div class="msgList">
    	<h1 class="title"></h1>
    	<ul>
    		<li></li>
    	</ul>
    </div>
    <MyFooter></MyFooter>
   </div>
</template>

<script>
import MyHeader from './../../components/header/index.vue';
import MyFooter from './../../components/footer/index.vue';

import yanchanghui from "./img/yanchanghui.png";
import yinyuehui from "./img/yinyuehui.png";
import hjgj from "./img/hjgj.png";
import qyzt from "./img/qyzt.png";
import tybs from "./img/tybs.png";
import etqz from "./img/etqz.png";
import wdbl from "./img/wdbl.png";

import Banner from './../../components/banner/index.vue';
export default {
  data () {
    return {
    goodList:['演唱会','音乐会','话剧歌剧','曲艺杂谈','体育比赛','儿童亲子','舞蹈芭蕾'],
    iconList:[yanchanghui,yinyuehui,hjgj,qyzt,tybs,etqz,wdbl],
    IsShow:false,
    Info:''
    }
  },
  mounted(){
  	this.getData();
  },methods:{
    show(index){
    	this.Info=index;
    	this.IsShow=!this.IsShow;
    },
    hide(index){
    	this.IsShow=!this.IsShow;
    },
    getData(){
    	
    }
  },
  components:{
       MyHeader,
       MyFooter,
       Banner
      
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.nav{
	background: #FFFFFF;
	margin: 20px 80px;
	height: 500px;
	position: relative;
}
.navbar{
	position: absolute;
	left: 130px;
	z-index: 1;
}
.navbar ul {
   height: 45px;
   line-height: 45px;
} 
.goodsList{
	width:200px;
	position: absolute; 
    top:0;
    left: 0;
	z-index: 2;
	text-align: center;	
}
.goodsList h3{
	background: #000;
	line-height: 45px;
	color: #fff;	
}
.goodsList ul{
	background: red;
	height: 420px;
}
.goodsList ul li{
     padding: 10px 0;
     list-style: none; 		
}
.goodsList ul li a{
	color: #fff;
}
.goodsList ul li:hover{
	background: darkred;
}
.goodsList ul li:hover a{
	color: #D3D3D3;
}
.goodsList ul li a img{
    position: absolute;
    left:25px;	
}
.goodsList ul li a span{
    position: absolute;
    right:15px;	
}
.goodsListDetail{
	width:800px;
	height: 420px;
	color: #000000;
	position:absolute;
	top:45px;
	left:200px;
	background:rgba(230,230,230,0.6);
	z-index: 10;
	
}
.carousel{
	width: 1000px;
	height:420px;
	position: absolute;
	top:45px;
	left:200px;
}
.carousel img{
	width:800px;
}
</style>