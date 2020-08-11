<template>
  <li  class="brick-item">
    <a :href="goods.href">
      <img :src="goods.img" alt class="figure-img" />
      <h3 class="title">{{goods.name}}</h3>
      <p class="desc">{{goods.jieshao}}</p>
      <p class="price">
        <span>{{goods.price}}元</span>
        <del v-show="goods.del_price">{{goods.del_price}}元</del>
      </p>
    </a>
  </li>
</template>

<script>
export default {
	props:['goods']
};
</script>

<style lang="less" scoped>
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
			margin: 0 auto 18px auto;
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
</style>