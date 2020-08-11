<template>
  <div class="header">
    <div class="navtop">
      <div class="container">
        <div class="site-topbar">
          <div class="topbar-nav">
            <template v-for="nav,index in top_nav">
              <a :href="nav.href" :key="index">{{nav.name}}</a>
              <span v-if="index!==11">|</span>
            </template>
          </div>
        </div>

        <div class="cart" @mouseenter="cart_show" @mouseleave="cart_hide">
          <a :class="{over: cartShow}" href="www.mi.com/buy/cart" >
            <em class="icon iconfont">&#xe63b;</em>
            <span>购物车（0）</span>
          </a>
          <div :class="cart_class" >
            <p v-show="cart_text_show">购物车中还没有商品</p>
          </div>
        </div>

        <div class="user">
          <template v-for="u,index in user">
            <a :href="u.href" :key="index">{{u.name}}</a>
            <span v-if="index!==2">|</span>
          </template>
        </div>
      </div>
    </div>
    <div class="site-header clearfix">
      <div class="header-logo">
        <a href="https://www.mi.com/index.html" title="小米官网">小米官网</a>
      </div>
      <div class="nav-list">
        <ul class="clearfix">
          <li class="nav-list-head">全部商品分类</li>
          <li v-for="item,index in header_nav" :key="index" @mouseenter="li_enter(item.name)" @mouseleave="nav_hide">
            <a href="#">{{item.name}}</a>
          </li>
        </ul>
      </div>
	  <div class="header-search">
		  <form class="search-form clearfix">
			  <a class="no-style-msq">
				  <input type="text" id="search" class="search-text" name="keyword" autocomplete="off" placeholder="耳机">
			  </a>
			  <a id="J_submitBtn" class="no-style-msq">
				  
				  <button type="submit" class="search-btn icon iconfont icon-icon-test2" ></button>
			  </a>

		  </form>
	  </div>
	  <div :class="header_nav_class">
		  <ul class="nav-item-menu clearfix">
			  <li v-for="item,index in nav_item" :key="index">
				  <a href="#">
					  <img :src="item.img" alt="" class="figure">
					  <div class="title">{{item.name}}</div>
					  <p class="price">{{item.price}}</p>
				  </a>
			  </li>
		  </ul>
	  </div>
    </div>
  </div>
</template>

<script>
export default {
	name: "HelloWorld",
	data() {
		return {
			cartShow: false,
			top_nav: [
				{ name: "小米商城", href: "www.mi.com/index.html" },
				{ name: "MIUI", href: "www.miui.com/" },
				{ name: "loT", href: "iot.mi.com" },
				{ name: "云服务", href: "i.mi.com/" },
				{ name: "金融", href: "jr.mi.com?from=micom" },
				{ name: "有品", href: "youpin.mi.com/" },
				{ name: "小爱开放平台", href: "xiaoai.mi.com/" },
				{ name: "企业团购", href: "qiye.mi.com/" },
				{ name: "资质证照", href: "www.mi.com/aptitude/list/?id=41" },
				{ name: "协议规则", href: "www.mi.com/aptitude/list/" },
				{ name: "下载app", href: "www.mi.com/appdownload/" },
				{ name: "Select Location", href: "#" },
			],
			user: [
				{ name: "登录", href: "#" },
				{ name: "注册", href: "#" },
				{ name: "消息通知", href: "#" },
			],
			header_nav: [
				{ name: "小米手机" },
				{ name: "Redmi 红米" },
				{ name: "电视" },
				{ name: "笔记本" },
				{ name: "家电" },
				{ name: "路由器" },
				{ name: "智能硬件" },
				{ name: "服务" },
				{ name: "社区" },
			],
			item_menu:{
				"小米手机":[
					{name:'小米10 Pro',price:'4999元起',img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82ddffd7562c54f9166fa876c143ff22.png?thumb=1&w=240&h=165'},
					{name:'小米10',price:'3699元起',img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/a4a76ee684e51f0ee531ef3dc7f0aeaf.png?thumb=1&w=240&h=165'},
					{name:'小米10 青春版 5G',price:'1899元起',img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=240&h=165'},
					{name:'小米MIX Alpha',price:'19999元',img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/5d19da60f9f62eb2aa5dcdbd7df19f0f.png?thumb=1&w=240&h=165'}
				],
				"Redmi 红米":[
					{name:'Redmi K30 Pro 系列',price:'2699元起',img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0203f4e7dafcc0c9016a1b48556abf30.jpg?thumb=1&w=240&h=165'},
					{name:'Redmi K30 系列',price:'1399元起',img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/cff2977b8aab1e43b94b2f00083f4ae1.jpg?thumb=1&w=240&h=165'},
					{name:'Redmi 10X 5G',price:'1599元起',img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/6a6548361871303764d6c66142074524.png?thumb=1&w=240&h=165'},
					{name:'Redmi Note 8',price:'899元起',img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/dacd6a3d8440b7a038e9778702bd6db6.png?thumb=1&w=240&h=165'}
				],
				"智能硬件":[
					{name:'小米米家智能摄像机云台版',price:'199元',img:'https://cdn.cnbj0.fds.api.mi-img.com/b2c-mimall-media/2a500be4264c692899b25d86c16403f7.jpg?thumb=1&w=240&h=165'},
					{name:'小米小爱老师',price:'399元起',img:'https://cdn.cnbj0.fds.api.mi-img.com/b2c-mimall-media/e3fb0886fdb13e5ae784b9713b9a0038.jpg?thumb=1&w=240&h=165'},
					{name:'小米米家智能门锁',price:'1299元起',img:'https://cdn.cnbj0.fds.api.mi-img.com/b2c-mimall-media/5630aa997c82409ee33b2814c7eb2244.jpg?thumb=1&w=240&h=165'},
					{name:'Redmi小爱触屏音箱 8',price:'349元',img:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/dccc32d8e36685485fa89e0f2a580975.png?thumb=1&w=240&h=165'}
				]
			},
			cart_class:[
				"cart-content",
				"cart-hide"
			],
			header_nav_class:[
				"header-nav-menu",
				"nav-hidden"
			],
			cart_text_show:false,
			nav_item:[]
		};
	},
	methods: {
		cart_show(){
			this.cart_class=["cart-content","cart-show"];
			setTimeout(() => {
				this.cart_text_show=true;
			}, 0.3);
			// console.log('in');
		},
		cart_hide(el){
			setTimeout(() => {
				this.cart_class=["cart-content","cart-hide"];
				this.cart_text_show=false;
			}, 0.3);
			// this.cart_class=["cart-content","cart-hide"];
			// this.cart_text_show=false;
			// el.display='none';
		},
		li_enter(item){
			this.nav_item=this.item_menu[item]||[];
			this.nav_show();
		},
		nav_show(){
			this.header_nav_class=["header-nav-menu","nav-show"];
		},
		nav_hide(){
			this.header_nav_class=["header-nav-menu","nav-hidden"];
		}
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.header {
	.navtop {
		background: #333;
		.container {
		width: 1226px;
		margin: 0 auto;
		// clear: both;
		color: #b0b0b0;
		background: #333;
			&::before,
			&::after {
				content: " ";
				clear: both;
				display: block;
			}
		}
	}
}
.site-topbar {
	position: relative;
	float: left;
	height: 40px;
	font-size: 12px;
	color: #b0b0b0;
	background: #333;
	a {
		display: inline-block;
		color: #b0b0b0;
		line-height: 40px;
		text-decoration: none;
	}
	span {
		margin: 0.3em;
		color: #424242;
	}
	&::before {
		content: " ";
		display: table;
	}
}
.cart {
	position: relative;
	display: block;
	float: right;
	width: 120px;
	height: 40px;
	margin-left: 15px;
	transition: all 0.2s;
	font-size: 12px;
	a {
		display: block;
		color: #b0b0b0;
		background: #424242;
		text-align: center;
		line-height: 40px;
		&.over {
			background: #fff;
			color: orange;
		}
		em {
			line-height: 20px;
			font-size: 20px;
			margin-right: 4px;
		}
	}
	.cart-content {
		position: absolute;
		right: 0;
		top: 40px;
		width: 316px;
		// height: 100px;
		background: #fff;
		z-index: 30;
		box-shadow: 0 2px 10px rgba(0, 0, 0.15);
		transition: height .3s;
		display: flex;
		p {
			text-align: center;
			// line-height: 100px;
			align-items: center;
			margin: auto;
			display: flex;
		}
	}
	.cart-hide {
		height: 0px;
		// display: none;
	}
	.cart-show {
		height: 100px;
	}
}
.user {
	position: relative;
	float: right;
	height: 40px;
	line-height: 40px;
	color: #b0b0b0;
	background: #333;
	font-size: 12px;
	a {
		padding: 0 5px;
		color: #b0b0b0;
	}
	span {
		margin: 0.3em;
		color: #424242;
	}
}

.site-header {
	width: 1226px;
	margin: 0 auto;
	position: relative;
	.header-logo {
		float: left;
		width: 62px;
		margin-top: 22px;
		
		// background-color: orange;
		a {
			// margin-left: -55px;
			position: relative;
			display: block;
			width: 55px;
			height: 55px;
			overflow: hidden;
			background: url(//s02.mifile.cn/assets/static/image/mi-home.png) no-repeat 50% 50%;
			background-color: #ff6700;
			text-indent: -999em;
			&::after,
			&::before {
				position: absolute;
				left: 0;
				top: 0;
				width: 55px;
				height: 55px;
				content: "";
				z-index: 1;
			}
		}
	}
	.nav-list {
		float: left;
		width: 850px;
		height: 100px;
		ul {
			width: 850px;
			height: 88px;
			margin: 12px 0 0 30px;
		}
	}
}

.nav-list li {
	display: inline-block;
	float: left;
	
	&.nav-list-head {
		width: 127px;
		opacity: 0;
	}
	a {
		display: block;
		padding: 26px 10px 38px;
		color: #333;
		transition: color 0.2s;
		font-size: 16px;
	}
}

.header-search {
	float: right;
	width: 296px;
	margin-top: 25px;
	// background-color: #333;
	.search-form {
		position: relative;
		width: 296px;
		height: 50px;
		z-index: 20;
		.search-text, .search-btn {
			position: absolute;
			top:0;
			border: 1px solid #e0e0e0;
			outline: 0;
			transition: all .2s;
		}
		.search-text {
			right: 51px;
			z-index: 1;
			width: 223px;
			height: 48px;
			padding: 0 10px;
			font-size: 14px;
			line-height: 48px;
		}
		.search-btn {
			right: 0;
			z-index: 2;
			width: 52px;
			height: 50px;
			font-size: 24px;
			line-height: 24px;
			background-color: #fff;
			color: #616161;
			// &::before {
			// 	content: "\e63d";
			// }
		}
	}
}
.header-nav-menu {
	position: absolute;
	top: 100px;
	left:0;
	display: block;
	z-index: 24;
	width: 100%;
	border-top: 1px solid #e0e0e0;
	background: #fff;
	overflow: hidden;
	height: 229px;
	transition: all .3s;
	&.nav-show {
		height: 229px;
	}
	&.nav-hidden {
		height: 0px;
	}
	.nav-item-menu {
		width: 1226px;
		margin: 0 auto;
		position: relative;
		li {
			position: relative;
			float: left;
			width: 180px;
			padding: 35px 12px 0;
			text-align: center;
			.figure {
				display: block;
				width: 160px;
				height: 110px;
				margin: 0 auto 16px;
			}
			.title {
				color: #333;
				margin: 0;
				line-height: 20px;
				font-size: 12px;
			}
			.price {
				margin: 0;
				line-height: 20px;
				color: #ff6700;
				font-size: 12px;
			}
			&:nth-child(n+1)::before {
				position: absolute;
				left: 0;
				top: 35px;
				width: 1px;
				height: 100px;
				content: '';
				background-color: #e0e0e0;
			}
		}
	}
}
</style>