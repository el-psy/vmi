<template>
  <div class="brick clearfix">
    <div class="box-hd clearfix">
      <h2 class="title">搭配</h2>
      <ul>
        <li>热门</li>
        <li>耳机音箱</li>
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
              <a href="https://www.mi.com/buy?product_id=12090">
                <img
                  src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/601d1ac94ca155a59a813bff1045e8b3.jpg?thumb=1&w=150&h=150"
                  alt
                />
                <h3 class="title">小米无线车充通用快充版</h3>
                <p>
                  <span>109</span>元
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
      <a href="https://www.mi.com/a/h/15274.html">
        <img
          src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9880db34d227b6c1df5b45cb7df4f465.jpg?thumb=1&w=1839&h=180"
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
					href: "https://www.mi.com/scooter/",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/6874615b3c50e837ffe532eb6ea4ef1a.jpg?thumb=1&w=351&h=450",
				},
				{
					href: "https://www.mi.com/buy?product_id=11191",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/a00bdd568dbc2b02f8fe0fa8d1b46f28.jpg?thumb=1&w=351&h=450",
				},
			],
			goods: [
				{
					name: "小米真无线蓝牙耳机 Air 2",
					jieshao: "智能真无线，轻松舒适戴",
					price: "299",
					del_price: "399",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/50649d7b5706f4cd9f658e93db6b6564.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=10859",
				},
				{
					name: "高速无线充套装",
					jieshao: "快速无线闪充，Qi充电标准",
					price: "149",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9eb0178e3bfeb7d170edd641fb4be4bc.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=9311",
				},
				{
					name: "Redmi充电宝 10000mAh 标准版 白色",
					jieshao: "10000mAh大电量 ",
					price: "59",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ea8e42faebf7d76a4cb42b8930cf9e46.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=10317",
				},
				{
					name: "Redmi充电宝 20000mAh 快充版",
					jieshao: "大容量，	可上飞机 ",
					price: "99",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/eaf70e0e9905de6452f07b1f48fcc386.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/buy?product_id=10318",
				},
				{
					name: "小米插线板 5孔位",
					jieshao: "多重安全保护",
					price: "39",
					img:
						"https://i8.mifile.cn/v1/a1/5dd69c0a-8f4a-b42f-d840-6c5a47f2cd03!300x300.jpg",
					href: "https://www.mi.com/buy?product_id=5857",
				},
				{
					name: "小米蓝牙耳机AirDots青春版",
					jieshao: "雅致简约，收纳充电盒",
					price: "199",
					img:
						"https://i8.mifile.cn/b2c-mimall-media/92af1f21293fabfbf2a112892b864925!300x300.jpg",
					href: "https://www.mi.com/buy?product_id=9016",
				},
				{
					name: '小米小爱触屏音箱',
					jieshao: "好听，更好看",
					price: "199",
					img:
						"https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9946e252a7c49662376c056ced004a20.jpg?thumb=1&w=300&h=300",
					href: "https://www.mi.com/aispeaker-touch/",
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