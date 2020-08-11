<template>
  <div id="ad" class="clearfix">
    <div class="ad-up clearfix">
      <div class="aside">
        <ul id="categoryList">
          <li v-for="item,index in aside" :key="index">
            <a :href="item.href">
              {{item.name}}
              <em class="iconfont icon-icon-test6"></em>
            </a>
          </li>
        </ul>
      </div>
      <div class="switch">
		  <div class="switch-div" v-for="item,index in swape" :key="index" v-if="swape_show==index">
			  <a class="switch-a" :href="item.href">
				  <img class="switch-img" :src="item.img" alt="">
			  </a>
		  </div>

	  </div>
    </div>
	<div class="ad-down clearfix">
		<div class="cubic">
			<ul class="clearfix">
				<li v-for="item,index in cub_list" :key="index">
					<a :href="item.href">
						<img :src="item.img" alt="">
						{{item.name}}
					</a>
				</li>
			</ul>
		</div>
		<div class="hero-left">
			<ul>
				<li v-for="item, index in ad_left" :key="index">
					<a :href="item.href">
						<img :src="item.img" alt="">
					</a>
				</li>
			</ul>
		</div>
	</div>
  </div>
</template>

<script>
export default {
	data() {
		return {
			aside: [
				{ name: "手机 电话卡", href: "https://www.mi.com/p/1915.html" },
				{ name: "电视 盒子", href: "https://www.mi.com/a/h/9819.html" },
				{ name: "笔记本 显示器", href: "https://www.mi.com/a/h/7529.html" },
				{ name: "家电 插线板", href: "https://www.mi.com/p/9285.html" },
				{ name: "出行 穿戴", href: "https://www.mi.com/p/9829.html" },
				{ name: "智能 路由器", href: "https://www.mi.com/a/h/8363.html" },
				{ name: "电源 配件", href: "https://www.mi.com/p/9290.html" },
				{ name: "健康 儿童", href: "https://www.mi.com/p/9291.html" },
				{ name: "耳机 音箱", href: "https://www.mi.com/p/9292.html" },
				{ name: "生活 箱包", href: "https://www.mi.com/p/9293.html" },
			],
			swape: [
				{
					href:'https://www.mi.com/a/h/16461.html',
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/a53a285c8c341dd27dd60db89c8f063e.jpg?thumb=1&w=1839&h=690",
				},
				{
					href:'https://www.mi.com/buy?product_id=10000240',
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/6ef43cf9f138a7fc3a39273d7e3d13b6.jpg?thumb=1&w=1839&h=690",
				},
				{
					href:'https://www.mi.com/washer-dryer-10/',
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9f1365c7a7d0070c1f71f5d797cf11fe.jpg?thumb=1&w=1839&h=690",
				},
			],
			cub_list:[
				{name:'小米秒杀', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82abdba456e8caaea5848a0cddce03db.png?w=48&h=48', href:'https://www.mi.com/buy/seckill'},
				{name:'企业团购', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/806f2dfb2d27978e33fe3815d3851fa3.png?w=48&h=48', href:'https://qiye.mi.com/'},
				{name:'F码通道', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/eded6fa3b897a058163e2485532c4f10.png?w=48&h=48', href:'https://www.mi.com/order/fcode'},
				{name:'米粉卡', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/43a3195efa6a3cc7662efed8e7abe8bf.png?w=48&h=48', href:'https://www.mi.com/mimobile/'},
				{name:'以旧换新', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f4846bca6010a0deb9f85464409862af.png?w=48&h=48', href:'https://huanxin.mi.com/'},
				{name:'话费充值', img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9a76d7636b08e0988efb4fc384ae497b.png?w=48&h=48', href:'https://recharge.10046.mi.com/'}
			],
			ad_left:[
				{img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/c0c05274f2fbb55fbccb89622f798907.jpg?w=632&h=340', href:'https://www.mi.com/buy?product_id=10000223'},
				{img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/b746a4db2e0473cc076a3a4b9bbe0235.jpg?w=632&h=340', href:'https://www.mi.com/buy?product_id=10000240'},
				{img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/816a66edef10673b4768128b41804cae.jpg?w=632&h=340', href:'https://www.mi.com/shouhuan4/'}
			],
			swape_show: 1
		};
	},
};
</script>

<style lang="less" scoped>
#ad {
	width: 1226px;
	margin-right: auto;
	margin-left: auto;
	position: relative;
	.aside {
		position: absolute;
		width: 234px;
		height: 460px;
		z-index: 1;
		// background-color: #eee;
	}
	.switch {
		position: relative;
		height: 460px;
		background-color: #eee;
	}
	.ad-down {
		margin-top: 14px;
		background-color: #eee;
	}
}

.aside {
	ul {
		margin: 0;
		padding: 20px 0;
		height: 420px;
		border: 0;
		color: #fff;
		background: rgba(105, 101, 101, 0.6);
		li {
			position: relative;
			display: block;
			padding-left: 30px;
			height: 42px;
			line-height: 42px;
			a {
				color: #fff;
			}
		}
	}
}

.switch {
	.switch-div {
		position: relative;
		width: 100%;
		height: 100%;
		display: inline-block;
	}
	.switch-img {
		width: 1226px;
		height: 460px;
		display: block;
	}
}

.ad-down {
	.cubic {
		width: 234px;
		float: left;
		// margin-left: 14px;
		min-height: 1px;
		ul {
			margin: 0;
			padding: 3px;
			font-size: 12px;
			text-align: center;
			background-color: #5f5750;
			li {
				position: relative;
				float: left;
				width: 70px;
				height: 82px;
				padding:0 3px;
				&::before {
					top: -1px;
					left: 6px;
					width: 64px;
					height: 1px;
				}
				&::after {
					top: 6px;
					left:0;
					width: 1px;
					height: 70px;
				}
				&::after, &::before {
					position: absolute;
					content: '';
					background-color: #665e57;
				}
				a {
					display: block;
					padding-top: 18px;
					color: #fff;
					opacity: .7;
					transition: opacity .2s;
					font-size: 12px;
					&:hover {
						opacity: 1;
					}
					img {
						width: 24px;
						height: 24px;
						display: block;
						margin: 0 auto 4px;
					}
				}
			}
		}
	}
}

.hero-left {
	width: 978px;
	float: left;
	margin-left: 14px;
	min-height: 1px;
	li {
		display: block;
		float: left;
		width: 316px;
		height: 170px;
		margin-left: 15px;
		&:first-child{
			margin-left: 0;
		}
		a {
			display: block;
			height: 170px;
			img {
				display: block;
				width: 316px;
				height: 170px;
			}
		}
	}
}
</style>