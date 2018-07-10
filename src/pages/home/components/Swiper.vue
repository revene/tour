<template>
	<div class="wrapper">
		<swiper :options="swiperOption">
	  		<swiper-slide v-for="item of swiperList" :key="item.id">
	    		<img class="swiper-img" :src="item.imgUrl" >
	    	</swiper-slide>
	    	<div class="swiper-pagination"  slot="pagination"></div>
	  </swiper>
	</div>
</template>

<script>
	export default {
		name:'HomeSwiper',
		data:function(){
			return {
				swiperOption:{
					pagination:'.swiper-pagination',
					loop:true
				},
				swiperList:[{
					id:'0001',
					imgUrl:'http://img1.qunarzz.com/piao/fusion/1807/c6/44fce1467be17702.jpg_750x200_406f5fc3.jpg'
				},{
					id:'0002',
					imgUrl:'http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg'
				}]
			}
		}
	}
</script>

<style lang='stylus' scoped>
	.wrapper >>> .swiper-pagination-bullet-active
		background: #fff 
	.wrapper
		width:100%
		height:0
		overflow:hidden
		padding-bottom: 31.25%
		background:#fff
		.swiper-img
			width:100%
			
</style>