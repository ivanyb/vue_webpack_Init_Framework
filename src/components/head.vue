<template>

	<div class="head">
		<div class="mui-slider">
			<div class="mui-slider-group mui-slider-loop">
				<div class="mui-slider-item mui-slider-item-duplicate">
					<a href="#" v-if="lunbos[1]">
						<img :src="lunbos[1].img" />
						<p class="mui-slider-title">{{lunbos[1].title}}</p>
					</a>
				</div>
				<div class="mui-slider-item" v-for="item in lunbos">
					<a :href="item.url">
						<img :src="item.img" />
						<p class="mui-slider-title">{{item.title}}</p>
					</a>
				</div>
				<div class="mui-slider-item mui-slider-item-duplicate">
					<a href="#" v-if="lunbos[0]"><img :src="lunbos[0].img" />
						<p class="mui-slider-title">{{lunbos[0].title}}</p>
					</a>
				</div>
			</div>

			<div class="mui-slider-indicator mui-text-right">
				<div class="mui-indicator mui-active"></div>
				<div class="mui-indicator"></div>
			</div>
		</div>
	</div>
</template>

<script>
	
	export default {
		props: {
			headdata: {
				type: Object
			}
		},
		data() {
			return {
				lunbos: []
			}
		},
		created() { //created钩子，当整个 这个vue组件加载完毕以后被调用
			//请求远程json数据
//			this.$http.get('http://127.0.0.1:9090/api/getlunbo')
//			this.$http.get('http://czdm.ittun.com/api/getlunbo')
//				.then((response) => {
//					this.lunbos = response.body;
//				});
		this.lunbos = [{"_id":"57fb9108843ea116a85c8a06","img":"http://ofv795nmp.bkt.clouddn.com/lunbo1.jpg","title":"每个月都来给红旅打赏下吧","url":"http://www.itcast.cn/subject/phoneweb/index.html"},{"_id":"57fb910d843ea116a85c8a07","img":"http://ofv795nmp.bkt.clouddn.com/lunbo2.jpg","title":"红旅动漫资源分享群开放啦！！！","url":"http://www.itcast.cn/subject/phoneweb/index.html"}];
		}
	}
</script>

<style>
	.head h1 {
		color: red;
	}
</style>