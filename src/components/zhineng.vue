<template>
  <div class="brick clearfix">
    <div class="box-hd clearfix">
      <h2 class="title">智能</h2>
      <ul>
        <li>热门</li>
        <li>安防</li>
        <li>出行</li>
      </ul>
    </div>
    <div class="box-bd">
      <div class="row">
        <div class="span4">
          <ul>
            <li v-for="item, index in left" :keys="index">
              <a :href="item.href">
                <img :src="item.img" alt />
              </a>
            </li>
          </ul>
        </div>
        <div class="span16">
          <ul>
            <goods v-for="item, index in goods" :keys="index" :goods="item"></goods>
            <li class="half">
              <a href="https://www.mi.com/buy?product_id=9686">
                <img
                  src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/550177d2e54387521bce9e78cb2949dd.jpg?thumb=1&w=150&h=150"
                  alt
                />
                <h3 class="title">小米体脂秤2</h3>
                <p>
                  <span>99</span>元
                </p>
              </a>
            </li>
            <li class="down-half">
              <div class="icon">
                <i class="icon iconfont icon-icon-test6"></i>
              </div>
              <div class="more">
                浏览更多
                <small>热门</small>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="banner">
      <a href="https://www.mi.com/a/h/16461.html">
        <img
          src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/426144725b9ed90ce6fd2d9c69a8aa64.jpg?thumb=1&w=1839&h=180"
          alt
        />
      </a>
    </div>
  </div>
</template>

<script>
import Goods from "./children/goods.vue";
export default {
	data() {
		return {
			left: [
				{
					href: "https://www.mi.com/camera-360/",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/45c23f5b9a927b2dc49c25277e07727c.jpg?thumb=1&w=351&h=450",
				},
				{
					href: "https://www.mi.com/buy?product_id=9285",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/a660ce095e8f553a9ed1515265f4e9fc.jpg?thumb=1&w=351&h=450",
				},
			],
			goods: [
				{
					name: "小米「小爱老师",
					jieshao: "英语提分利器",
					price: "399",
					del_price: "499",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/011dd8493ad62f3793dbb63d9fbd3bc0.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/aiteacher-wifi/",
				},
				{
					name: "小米智能门锁 E",
					jieshao: "告别钥匙，畅享便捷生活",
					price: "989",
					del_price: "999",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f0914c60fa1ab807972541b4e2b1a4cd.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=12147",
				},
				{
					name: "小米小爱音箱 Play",
					jieshao: "听音乐、语音遥控家电",
					price: "99",
					del_price: "169",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e7c6e79433c883e1a022ec21402c1679.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/aispeaker-play/",
				},
				{
					name: "小爱音箱万能遥控版",
					jieshao: "传统家电秒变智能",
					price: "149",
					del_price: "199",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/44a30f0da2aacb66a0f896293ebc703f.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/aispeaker-control/",
				},
				{
					name: "米家电饭煲4L",
					jieshao: "890W 立体加热 ",
					price: "249",
					del_price: "299",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/b42e49c6c0208f2de5a2f7a491a3af46.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=9990",
				},
				{
					name: '小米手环4',
					jieshao: "大屏彩显，20天超长续航",
					price: "149",
					del_price: "169",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e850fa029579ba886e3d5c81f00ae534.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/shouhuan4/",
				},
				{
					name: "米家智能窗帘",
					jieshao: "窗帘开合随心控",
					price: "799",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3accd497afc0047cfbd40f442e3b17df.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=12274",
				},
			],
		};
	},
	components: {
		goods: Goods,
	},
};
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