<template>
	<div class="brick clearfix">
		<div class="box-hd clearfix">
			<h2 class="title">家电</h2>
			<ul>
				<li>热门</li>
				<li>电视影音</li>
			</ul>
		</div>
		<div class="box-bd">
			<div class="row">
				<div class="span4">
					<ul>
						<li v-for="item, index in left" :keys="index">
							<a :href="item.href">
								<img :src="item.img" alt="">
							</a>
						</li>
					</ul>
				</div>
				<div class="span16">
					<ul>
						<goods v-for="item, index in goods" :keys="index" :goods="item"></goods>
						<li class="half">
							<a href="http://www.mi.com/mibook/air13-2019">
								<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/74e573c4c0d89048392d14831cc507d5.jpg?thumb=1&w=150&h=150" alt="">
								<h3 class="title">Air 13.3" 2019款</h3>
								<p><span>5699</span>元起</p>
							</a>
						</li>
						<li class="down-half">
							<div class="icon">
								<i class="icon iconfont icon-icon-test6"></i>
							</div>
							<div class="more">
								浏览更多
								<small>电视影音</small>
							</div>
						</li>
					</ul>
				</div>
			</div>
		</div>
		<div class="banner">
			<a href="https://www.mi.com/buy?product_id=10025">
				<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/59e8fc8ba9718c266882719fb4bbcedd.jpg?thumb=1&w=1839&h=180" alt="">
			</a>
		</div>
	</div>
</template>

<script>
import Goods from './children/goods.vue'
export default {
	data(){
		return {
			left:[
				{href:'https://www.mi.com/buy?product_id=12159', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f256b81e4233333692eece77ed06ebc2.jpg?thumb=1&w=351&h=450'},
				{href:'https://www.mi.com/buy?product_id=11843', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e22cf675726deb5eb728f2ccd4cbeafd.jpg?thumb=1&w=351&h=450'}
			],
			goods:[
				{name:'Redmi 红米电视 70英寸', jieshao:'70英寸震撼巨屏，4K画质，细腻如真', price:'2999', del_price:'3799', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ef4c68fed730ec26bf2fa0ff620975c5.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/redmitv/70'},
				{name:'小米全面屏电视E32C', jieshao:'全面屏设计，人工智能系统', price:'699', del_price:'899', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/8b3fe3a07ef69fb4c959e39c768c7525.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/mitvall-screen/e32c/'},
				{name:'小米全面屏电视E55A', jieshao:'全面屏设计，人工智能语音', price:'1799', del_price:'1999', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ef6b4e9b9151849b3b1fb1dbf069c6ed.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/mitvall-screen/e55a/'},
				{name:'米家空调', jieshao:'出众静音，快速制冷热', price:'1499', del_price:'1799', img:'https://cdn.cnbj0.fds.api.mi-img.com/b2c-mimall-media/2b911be4c2f156bb6e4cf367c6080045.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/aircondition/f3w1/'},
				{name:'米家互联网洗烘一体机 Pro 10kg', jieshao:'智能洗烘，省心省力', price:'2999', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ec20453216dcd42f982cffe5fdbc3115.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/buy?product_id=9963'},
				{name:'Redmi全自动波轮洗衣机1A 8kg', jieshao:'一键操作，父母都爱用', price:'849', del_price:'899', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/b8c63a2024528fe5410ebe669b7d2407.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/buy?product_id=9509'},
				{name:'15.6" 四核i7 16G 独显 512G', jieshao:'全面均衡的国民轻薄本', price:'4699', del_price:'4899', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/cd2aa2dcad6440b469c22e27db9b6236.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/buy?product_id=10253'}
			]
		}
	},
	components: {
		'goods':Goods
	}
}
</script>

<style lang="less" scoped>
	.brick {
		.box-hd {
			.title {
				margin: 0;
				float: left;
				font-size: 22px;
				line-height: 58px;
				font-weight: 200;
				color: #333;
			}
			ul {
				margin: 0;
				padding: 16px 0 0 0;
				font-size: 16px;
				float: right;
				li {
					display: inline-block;
					margin: 0 0 0 30px;
					padding: 0;
				}
			}
		}
	}
	.span4 {
		width: 234px;
		float: left;
		// margin: 0 0 0 14px;
		min-height: 1px;
		ul {
			// margin: 0 0 -14px -14px;
			li {
				margin-bottom: 14px;
				height: 300px;
				padding: 0;
				// margin: 0 0 14px 14px;
				a {
					display: block;
					width: 100%;
					height: 100%;
					img {
						height: 300px;
						width: 234px;
					}
				}
			}
		}
	}
	.span16 {
		margin: 0 0 0 14px;
		li.half {
			height: 93px;
			padding-top: 50px;
			position: relative;
			float: left;
			width: 234px;
			margin-left: 14px;
			margin-bottom: 14px;
			background: #fff;
			a {
				// color: #757575;
			}
			img {
				position: absolute;
				right: 20px;
				top: 32px;
				width: 80px;
				height: 80px;
			}
			h3.title {
				margin: -10px 110px 5px 30px;
				font-size: 14px;
				font-weight: 400;
				color: #333;
			}
			p {
				margin: 0 110px 0 30px;
				font-size: 12px;
				color: #ff6700;
				span {
					font-size: 14px;
				}
			}
		}
		li.down-half {
			position: relative;
			height: 93px;
			padding-top: 50px;
			float: left;
			width: 234px;
			margin-left: 14px;
			margin-bottom: 14px;
			background-color: #fff;
			div.icon {
				position: absolute;
				right: 35px;
				top: 48px;
				width: 48px;
				height: 48px;
				color: #ff6700;
				i {
					font-size: 48px;
					line-height: 48px;
				}
			}
			div.more {
				display: block;
				margin: 0 110px 0 30px;
				font-size: 18px;
				color: #333;
				small {
					display: block;
					font-size: 12px;
					color: #757575;
				}
			}
		}
	}
	.banner {
		width: 1226px;
		height: 120px;
		margin: 22px 0;
		overflow: hidden;
		img {
			width: 100%;
			height: 100%;
		}
	}
</style>