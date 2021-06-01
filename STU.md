### 去掉字符串最后一位
	str.substr(0,str.length-1);

### 设置0.5px下划线
	&:before{
		content:'';
		position:absolute;
		left:0;
		right:0;
		bottom:1px;
		background-color:#CCC;
		transform:scaleY(.5);
	}

### 动态路由传参方式有两种
	1. query传参，query?name=lance
	-- 获取参数 this.$route.query	
	2. rest传参，params/lance/123，路由配置: path:'params/:name/:age'
	-- 获取参数 this.$route.params

### 路由守卫分三种
	1. 全局守卫
	router.beforeEach((to,from,next)=>{
		next();
	})
	2. 路由独享守卫
	routes: [{
      path: '/foo',
      component: Foo,
      beforeEnter: (to, from, next) => {
      }
    }]
    3. 组件内守卫
    const Foo = {
  		template: ``,
  		beforeRouteEnter(to, from, next) {},
	  	beforeRouteUpdate(to, from, next) {},
	  	beforeRouteLeave(to, from, next) {}
	}

### 自定义指令
	Vue.directive('focus', {
		bind:function(el){},
	  	inserted:function(el){
	    	el.focus()
	  	},
	  	undate:function(el){}
	})
	-- 使用 <input v-focus>