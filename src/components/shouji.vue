<template>
	<div class="brick clearfix">
		<div class="box-hd">
			<h2 class="title">手机</h2>
			<div class="more">
				<a href="https://www.mi.com/a/h/14933.html">
					查看全部
					<i class="iconfont icon-icon-test6"></i>
				</a>
			</div>
		</div>
		<div class="box-bd clearfix">
			<div class="row">
				<div class="span4">
					<a href="https://www.mi.com/mixalpha">
						<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/574c6643ab91c6618bfb2d0e2c761d0b.jpg?thumb=1&w=351&h=921" alt="">
					</a>
				</div>
				<div class="span16">
					<ul class="brick-list clearfix">
						<li v-for="item,index in goods" :key="index" class='brick-item'>
							<a :href="item.href">
								<img :src="item.img" alt="" class='figure-img' >
								<h3 class="title">{{item.name}}</h3>
								<p class="desc">{{item.jieshao}}</p>
								<p class="price">
									<span>{{item.price}}元</span>
									<del v-show="item.del_price">{{item.del_price}}元</del>
								</p>
							</a>
							
						</li>
					</ul>
				</div>
			</div>
		</div>
		<div class="banner-box">
			<a href="https://www.mi.com/a/h/15707.html" target="_blank">
				<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/c3b86ede4dd31d7c126d56fbdde4f855.jpg?thumb=1&w=1839&h=180" alt="">
			</a>
		</div>
	</div>
</template>

<script>
export default {
	data(){
		return {
			goods:[
				{name:'Redmi 9A', jieshao:'5000mAh长循环大电量，6.53"超大护眼屏幕', price:'599', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/c892a7640f58032489cbff8a948b50f9.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/redmi9a'},
				{name:'小米10 青春版 5G', jieshao:'50倍潜望式变焦 / 轻薄5G手机', price:'1899', del_price:'2099', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/8729282b199b3ec51e31c1b6b15f3f93.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/mi10youth'},
				{name:'小米10', jieshao:'骁龙865/1亿像素相机', price:'3799', del_price:'3999', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0099822e42b4428cb25c4cdebc6ca53d.jpg?thumb=1&w=300&h=300', href:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0099822e42b4428cb25c4cdebc6ca53d.jpg?thumb=1&w=300&h=300'},
				{name:'Redmi K30 Pro', jieshao:'双模5G，骁龙865，弹出全面屏', price:'2499', del_price:'2699', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/c1aafa589258a4d9fdf49831b457418d.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/buy?product_id=10000223'},
				{name:'Redmi K30 Pro 变焦版', jieshao:'双模5G，骁龙865，弹出全面屏', price:'3799', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/7cfdbce40301133a287e9e57faa37bdf.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/buy?product_id=11763'},
				{name:'小米10 Pro', jieshao:'骁龙865 / 50倍变焦', price:'4999', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ccd09671448c4cdb4a3817f68f788662.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/buy?product_id=10000213'},
				{name:'Redmi K30', jieshao:'120Hz流速屏，全速热爱', price:'1399', del_price:'1699', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/2c16238f786e4f93bdb175d7bf21aa47.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/buy/detail?product_id=10000203'},
				{name:'Redmi K30 5G', jieshao:'双模5G，120Hz流速屏', price:'1699', del_price:'2299', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/53641901fbc28cbcdb495b17fdf69e46.jpg?thumb=1&w=300&h=300', href:'https://www.mi.com/buy/detail?product_id=10000204'}
			]
		}
	}
}
</script>

<style lang="less" scoped>
	.brick {
		margin-top: 8px;
		.box-hd {
			position: relative;
			height: 58px;
		}
		.box-bd {
			.row {
				// margin-left: -14px;
				.span4 {
					width: 234px;
					float: left;
					// margin-left: 14px;
					min-height: 1px;
				}
				.span16 {
					width: 978px;
					float: left;
					margin-left: 14px;
					min-height: 1px;
				}
			}
		}
	}
	h2.title {
		margin: 0;
		font-size: 22px;
		font-weight: 200;
		line-height: 58px;
		color: #333;
	}
	.more {
		position: absolute;
		top: 0;
		right: 0;
		a {
			font-size: 16px;
			line-height: 58px;
			color: #424242;
			i {
				padding: 4px;
				margin-left: 8px;
				border-radius: 16px;
				font-size: 12px;
				line-height: 12px;
				background: #b0b0b0;
				color: #fff;
				vertical-align: 1px;
			}
		}
	}
	.span4 {
		a {
			display: block;
			width: 100%;
			height: 614px;
			// margin: 0 0 -14px -14px;
			img {
				width: 100%;
				height: 100%;
			}
		}
	}
	.span16 {
		ul {
			margin: 0 0 -14px -14px;
			li {
				float: left;
				display: block;
				width: 234px;
				height: 260px;
				margin: 0 0 14px 14px;
				padding: 20px 0;
				background: #fff;
				a {
					display: block;
					img {
						width: 160px;
						height: 160px;
						display: block;
						margin: 0 auto;
					}
					.title {
						margin: 0 10px 2px 10px;
						text-align: center;
						font-size: 14px;
						font-weight: 400;
						color: #333;
					}
					.desc {
						margin: 0 10px 10px 10px;
						height: 18px;
						font-size: 12px;
						color: #b0b0b0;
						text-align: center;
						overflow: hidden;
						text-overflow: ellipsis;
						white-space: nowrap;
					}
					.price {
						margin: 0 10px 14px;
						text-align: center;
						color: #ff6700;
						del {
							color: #b0b0b0;
							margin: 0 0 0 7px;
						}
					}
				}
			}
		}
	}
	.banner-box {
		margin: 22px 0;
		height: 120px;
		img {
			width: 1226px;
			height: 120px;
		}
	}
</style>