<template>
	<div class="footer">
		<div class="site-footer">
			<div class="footer-service">
				<ul class="clearfix">
					<li v-for="item, index in service" :key="index">
						<a :href="item.href">{{item.name}}</a>
					</li>
				</ul>
			</div>
			<div class="footer-links clearfix">
				<dl v-for="dl_link, dl_index in links" :key="dl_index">
					<dt>{{dl_link.name}}</dt>
					<dd v-for="link, link_index in dl_link.links" :key="link_index">
						<a :href="link.href">{{link.name}}</a>
					</dd>
				</dl>
				<div class="contact">
					<p class="phone">400-100-5678</p>
					<p>8:00-18:00(仅收市话费)</p>
					<a href="#" class="fuwu">
						<em class="icon iconfont icon-icon-test1"></em>
						人工服务
					</a>
					<div class="follow">
						关注小米:
						<a href="https://weibo.com/xiaomishangcheng"></a>
						<a href="javascript:void(0);"></a>
					</div>
				</div>
			</div>
		</div>
		<div class="site-info">
			<div class="logo">小米官网</div>
			<div class="indo-text">
				<p class="sites">
					<template v-for="site, index in infos">
						<a href="#"  :key="index">
							{{site}}
						</a>
						<span v-show="index!==13">|</span>
					</template>
				</p>
				<p>
					<a href="#" v-for="item, index in foot_1" :key="index">{{item}} </a>
					<br>
					<a href="#" v-for="item, index in foot_2" :key="index+5">{{item}} </a>
					<br>
					<a href="#">增值电信业务许可证</a>
					网络食品经营备案（京）【2018】WLSPJYBAHF-12
					<a href="#">食品经营许可证</a>
					<br>
					违法和不良信息举报电话：171-5104-4404 
					<a href="#">知识产权侵权投诉</a>
					本网站所列数据，除特殊说明，所有数据均出自我司实验室测试 
				</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data(){
		return {
			service: [
				{name:'预约维修服务', href:'https://www.mi.com/service/quick-repair'},
				{name:'7天无理由退货', href:'https://www.mi.com/service/exchange#back'},
				{name:'15天免费换货', href:'https://www.mi.com/service/exchange#back'},
				{name:'满99元包邮', href:'https://www.mi.com/service/buy/Postal%20policy'},
				{name:'520余家售后网点', href:'https://www.mi.com/static/maintainlocation/'}
			],
			links: [
				{name:'帮组中心', links:[
					{name:'账户管理', href:'https://www.mi.com/service/account/Account%20registration/'},
					{name:'购物指南', href:'https://www.mi.com/service/buy/SalesTime/'},
					{name:'订单操作', href:'https://www.mi.com/service/order/sendprogress/'}
				]},
				{name:'服务支持', links:[
					{name:'售后服务', href:'https://www.mi.com/service/exchange'},
					{name:'自助服务', href:'https://www.mi.com/service/'},
					{name:'相关下载', href:'https://www.mi.com/c/service/download/'}
				]},
				{name:'线下门店', links:[
					{name:'小米之家', href:'https://www.mi.com/c/xiaomizhijia/'},
					{name:'服务网点', href:'https://www.mi.com/static/maintainlocation/'},
					{name:'授权体验店', href:'https://www.mi.com/static/familyLocation/'}
				]},
				{name:'关于小米', links:[
					{name:'了解小米', href:'https://www.mi.com/about/'},
					{name:'加入小米', href:'https://hr.xiaomi.com/'},
					{name:'投资者关系', href:'https://company.mi.com/zh-cn/ir/indexContent/index.html'},
					{name:'企业社会责任', href:'https://www.mi.com/csr/'},
					{name:'廉洁举报', href:'https://integrity.mi.com/'}
				]},
				{name:'关于我们', links:[
					{name:'新浪微博', href:'https://weibo.com/xiaomishangcheng'},
					{name:'官方微信', href:'javascript:void(0);'},
					{name:'联系我们', href:'https://www.mi.com/about/contact/'},
					{name:'公益基金会', href:'https://www.mi.com/foundation/index'}
				]},
				{name:'特色服务', links:[
					{name:'F 码通道', href:'https://www.mi.com/order/fcode'},
					{name:'礼物码', href:'https://www.mi.com/order/giftcode'},
					{name:'防伪查询', href:'https://www.mi.com/service/imei'}
				]}
			],
			infos: ['小米商城', 'MIUI', '米家', '米聊', '多看', '游戏', '政企服务', '小米天猫店', '小米集团隐私政策', '小米公司儿童信息保护规则', '小米商城隐私政策', '小米商城用户协议', '问题反馈', 'SelectLocation'],
			foot_1:['© mi.com', '京ICP证110507号', '京ICP备10046444号', '京公网安备11010802020134号', '京网文[2020]0276-042号'],
			foot_2:['（京）网械平台备字（2018）第00005号', '互联网药品信息服务资格证', '(京)-非经营性-2014-0090', '营业执照', '医疗器械质量公告']
		}
	}
}
</script>

<style lang="less" scoped>
	.footer {
		width: 1226px;
		margin: 0 auto;
	}
	.site-footer {
		margin: 0 auto;
		.footer-service {
			padding: 27px 0;
			border-bottom: 1px solid #e0e0e0;
			li {
				float: left;
				width: 19.8%;
				height: 25px;
				font-size: 16px;
				line-height: 25px;
				text-align: center;
				border-left: 1px solid #e0e0e0;
				&:first-child {
					border-left: none;
				}
				a {
					color: #616161;
					transition: color .2s;
					&:hover {
						color: #ff6700;
					}
				}
			}
		}
		.footer-links {
			padding: 40px 0;
			dl {
				width: 160px;
				height: 112px;
				float: left;
				margin: 0;
				dt {
					margin: -1px 0 26px;
					font-size: 14px;
					line-height: 1.25;
					color: #424242;
				}
				dd {
					margin: 10px 0 0;
					font-size: 12px;
					a {
						color: #757575;
						&:hover {
							color: #ff6700;
						}
					}
				}
			}
		}
	}
	.contact {
		p {
			margin: 0 0 5px 0;
			font-size: 12px;
		}
		.phone {
			font-size: 22px;
			line-height: 1;
			color: #ff6700;
		}
		.fuwu {
			border: 1px solid #ff6700;
			background: #fff;
			color: #ff6700;
			width: 118px;
			height: 28px;
			font-size: 12px;
			line-height: 28px;
			display: inline-block;
			padding: 0;
			margin: 0;
			text-align: center;
			transition: all .4s;
			&:hover {
				background: #ff6700;
				color: #fff;
			}
		}
		.follow {
			font-size: 12px;
			margin-top: 10px;
			position: relative;
			a {
				width: 24px;
				height: 24px;
				display: inline-block;
				vertical-align: middle;
				margin-left: 6px;
				margin-top: -3px;
				&:hover {
					background-color: #ff6700;
				}
				&:nth-child(1) {
					background: url(https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wb.png) 50% 0 no-repeat;
					background-size: cover;
				}
				&:nth-child(2) {
					background: url(https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wx.png) 50% 0 no-repeat;
					background-size: cover;
				}
			}
		}
	}
	.site-info {
		.logo {
			text-indent: -999em;
		}
		a {
			color: #757575;
			&:hover {
				color: #ff7600;
			}
		}
	}
</style>