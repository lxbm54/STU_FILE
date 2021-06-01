### HTML
#### 路由触发
	<router-link to="/foo"></router-link>
#### 路由出口
	<router-view></router-view>
	-- 路由匹配的组件渲染到这里

### JS
#### 定义路由组件
	const Foo = { template: '<div>foo</div>' }
#### 定义路由
	const routes = [{ path: '/foo', component: Foo }]
	-- 每个路由映射一个组件
#### 创建router实例，配置路由
	const router = new VueRouter({
  		routes
	})
#### 注入路由到根实例
	const app = new Vue({
  		router
	}).$mount('#app')

### 访问
	this.$router 访问路由器
	this.$route 访问当前路由