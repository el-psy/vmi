<template>
  <div class="brick clearfix">
    <div class="box-hd clearfix">
      <h2 class="title">配件</h2>
      <ul>
        <li>热门</li>
        <li>充电器</li>
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
              <a href="https://www.mi.com/powerstrip/">
                <img
                  src="https://cdn.cnbj0.fds.api.mi-img.com/b2c-mimall-media/d6484113b03acde1672d50c395c09763.jpg?thumb=1&w=150&h=150"
                  alt
                />
                <h3 class="title">小米插线板（含3口USB 2A快充）</h3>
                <p>
                  <span>49</span>元
                </p>
              </a>
            </li>
            <li class="down-half">
              <div class="icon">
                <i class="icon iconfont icon-icon-test6"></i>
              </div>
              <div class="more">
                浏览更多
                <small>充电器</small>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="banner">
      <a href="https://www.mi.com/buy?product_id=11674">
        <img
          src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ddec858a9371b4d7833181941520bf8b.jpg?thumb=1&w=1839&h=180"
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
					href: "https://www.mi.com/buy?product_id=9016",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/739ebd8abfc2b1be8866a2c1ad87e709.jpg?thumb=1&w=351&h=450",
				},
				{
					href: "https://www.mi.com/dispenser/",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ffe4182f1d9a5befdf2380ec90ae1620.jpg?thumb=1&w=351&h=450",
				},
			],
			goods: [
				{
					name: "小米Type-C充电器65W 疾速闪充版",
					jieshao: "疾速闪充",
					price: "99",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/971da2015fe533acebbca413f88084ab.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=12176",
				},
				{
					name: "小米GaN充电器 Type-C 65W",
					jieshao: "氮化镓黑科技 65W MAX 大功率快充",
					price: "149",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f8fde8a877fd4b12ad88119d9b6bc061.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=11543",
				},
				{
					name: "小米立式风冷无线充 30W",
					jieshao: "解锁充电新姿势",
					price: "199",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/15ac53312f850bfcc73bdc5a185fda8a.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=10860",
				},
				{
					name: "小米立式无线充电器 通用快充20W",
					jieshao: "横竖可充，迅速感应边充边玩",
					price: "79",
					del_price:'99',
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/bb115b0d5e6cc24c39c1ae818b63bf1a.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=11226",
				},
				{
					name: "小米无线充电器（通用快充）",
					jieshao: "铝合金外观，金属质感好",
					price: "69",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/69167d20371cb65e58ad792494d5bf63.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=11483",
				},
				{
					name: "米家智能插座蓝牙网关版",
					jieshao: "让传统家电变智能",
					price: "69",
					del_price:'79',
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/c85b67f1c4f5e460a4be5cea5858264b.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=11384",
				},
				{
					name: '米家插线板6位基础版（含3口USB 2A快充）',
					jieshao: "小巧设计，便捷不占地儿",
					price: "79",
					img:
						"https://cdn.cnbj0.fds.api.mi-img.com/b2c-miapp-a1/554198af-55ec-8400-7a04-66a8f3e0dd66.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/powerstrip6/",
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