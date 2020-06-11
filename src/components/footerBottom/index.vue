<template>
    <div class="footer-bottom">
    <Row type="flex" justify="center">
        <Col span="16">
            <Breadcrumb separator="|">
                <BreadcrumbItem v-for="i in info" to="/"> {{i}} </BreadcrumbItem>
            </Breadcrumb>
        </Col>
    </Row>
    <Row type="flex" justify="center" align="bottom">
        <Col span="3" v-for="u in url">
            <img :src="u"/>
        </Col>
    </Row>
    </div>
</template>

<script>
import icon_1 from "./images/icon_1.png";
import icon_2 from "./images/icon_2.png";
import icon_3 from "./images/icon_3.png";
import icon_4 from "./images/icon_4.png";
import icon_5 from "./images/icon_5.png";
import icon_6 from "./images/icon_6.png";
export default{
    name:'FootBottom',
    data(){
        return{
            info:
                [
                    '公司介绍',
                    '品牌识别',
                    '企业荣誉',
                    '隐私声明',
                    '联系及合作',
                    '招聘信息',
                    '网站地图',
                    '友情链接',
                    '公司大事记'
                ],
            url:
                [ 
                    icon_1,
                    icon_2,
                    icon_3,
                    icon_4,
                    icon_5,
                    icon_6 
                ]
        }
    }
}
</script>

<style scoped>
.footer-bottom{
    padding:10px;
}
.footer-bottom span{
    font-size:14px;
    font-weight:bold;
    padding-right:5px;
}
</style>