<template>
     <Carousel autoplay v-model="value" loop>
        <CarouselItem>
            <div class="demo-carousel">
            	<img src="./img/img1.jpeg"/>
            </div>
        </CarouselItem>
        <CarouselItem>
            <div class="demo-carousel">
            	<img src="./img/img2.jpg"/>
            </div>
        </CarouselItem>
        <CarouselItem>
            <div class="demo-carousel">
            	<img src="./img/img3.jpg"/>
            </div>
        </CarouselItem>
        <CarouselItem>
            <div class="demo-carousel">
            	<img src="./img/img4 (1).jpg"/>
            </div>
        </CarouselItem>
    </Carousel>
</template>

<script>
export default {
  name: 'Banner',
   data () {
            return {
                value: 0
            }
        }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.demo-carousel img{
	width:1000px;
    height: 420px;
}
</style>