### VUE常用安装
#### 生产环境依赖
	cnpm i axios -S
	cnpm i element-ui -S
	cnpm i echarts@4 -S
	cnpm i hex-sha1 -S
	cnpm i md5 -S
	cnpm i vue-amap --save
	-- 高德地图
	cnpm i vue-drag-verify --save
	-- 登陆验证

#### 开发环境依赖
	cnpm i node-sass@4 sass-loader@7 -D
	-- SCSS安装
	{
		test: /\.scss$/,
		loaders: ['style', 'css', 'sass']
	}