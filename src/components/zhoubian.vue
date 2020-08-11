<template>
  <div class="brick clearfix">
    <div class="box-hd clearfix">
      <h2 class="title">周边</h2>
      <ul>
        <li>热门</li>
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
              <a href="https://www.mi.com/buy?product_id=6512">
                <img
                  src="https://i8.mifile.cn/v1/a1/eaa7c8e5-2a8c-0d2c-6de7-a6db2068b192!150x150.jpg"
                  alt
                />
                <h3 class="title">8H 乳胶弹簧静音床垫 M3</h3>
                <p>
                  <span>1599</span>元起
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
      <a href="https://www.mi.com/buy?product_id=9836">
        <img
          src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/88e35cffc82cd98cd53172460067af17.jpg?thumb=1&w=1839&h=180"
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
					href: "https://www.mi.com/buy?product_id=10936",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/37dc0898c2624b4130da4631f2d9a675.jpg?thumb=1&w=351&h=450",
				},
				{
					href: "https://www.mi.com/buy?product_id=11674",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/582984b9c56cf3c48382a81528a4dfdf.jpg?thumb=1&w=351&h=450",
				},
			],
			goods: [
				{
					name: "米家飞行员太阳镜 Pro",
					jieshao: "尼龙偏光，轻巧佩戴",
					price: "199",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/cccac948e1b8ffb47f1fecde67692e60.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=9732",
				},
				{
					name: "小米巨能写中性笔10支装",
					jieshao: "一支顶4支，超长顺滑书写",
					price: "9.99",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/57433a4b991b2a2ddc889f2d8d434655.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=9836",
				},
				{
					name: "小米旅行箱 20英寸 布朗熊限量版",
					jieshao: "“国际巨星” LINE FRIENDS布朗熊",
					price: "299",
					del_price:'399',
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/c149537ebb0c2cdb977ddd93200074f4.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=10007",
				},
				{
					name: "米家迷你保温杯",
					jieshao: "可以随身携带的温度",
					price: "49",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/03d94ee6059481a6adcb6c4c5c572fb4.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=10480",
				},
				{
					name: "米家驱蚊器基础版 3个装",
					jieshao: "3个装 长效驱蚊",
					price: "99",
					del_price:'129',
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/41e6890f9d6b7fdb4275c986dc3644e8.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=9723",
				},
				{
					name: "卷装抽绳式垃圾袋",
					jieshao: "让清洁更简单",
					price: "9.9",
					del_price:'14.9',
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/38748fefeef78183ac01356a23dbc5c5.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=9938",
				},
				{
					name: '贝医生巴氏牙刷 四色装',
					jieshao: "进口刷毛，好品质",
					price: "39.9",
					img:
						"https://i8.mifile.cn/v1/a1/413f5e2f-53e7-0879-119c-8b4466feea53!300x300.jpg",
					href: "https://www.mi.com/toothbrush-set/",
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