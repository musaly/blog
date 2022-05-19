### 脚手架结构

1. node_modules 项目依赖
2. src 源文件
   1. assets 静态资源。webpack打包时候当作模块打包在js中
   2. components 全局组件，非路由组件
   3. App.vue唯一根组件
   4. main.js入口文件，最先执行
   5. pages 路由组件
3. babel.config.js 配置文件 Babel相关，一般不碰
4. package-lock.json 依赖缓存文件
5. package.json 项目身份证，项目名称依赖如何运行
6. README.md 说明文件
7. vue.config.js

项目完成时候自动打开主页
```package.json
"serve": "vue-cli-service serve"
"serve": "vue-cli-service serve --open" 自动打开
```

关闭校验工具
```vue.config.js
module.exports = {
    lintOnSave: false,
}
```

重命名路径


### 项目路由
vue-router
npm install --save vue-router@3
路由分析
非路由组件 header footer
路由组件 home search login register
$route 获取路由信息
$router 路由导航跳转
重定向

路由跳转
1. 声明式 router-link
2. 编程式 push|replace

路由参数
1. params 路径一部分，需要占位 占位后面加?代表可传可不传
2. query 不是路径一部分
3. 字符串，模板字符串传参
4. 对象传
5. props方式，
   1. 布尔值；传递的是params 参数
   2. 对象：传递额外数据
   3. 函数：可以传递 params query 

footer 组件显示和隐藏
1. this.$route.path 配合计算属性
2. 路由元信息

### 样式分析
识别less样式
npm install --save less less-loader@6
清除默认样式
组件创建注册引入


### 组件拆分
1. 三级联动组件，注册全局组件

### 接口
postman
http://39.98.123.211/api/product/getBaseCategoryList

npm install --save axios
axios二次封装
请求拦截器：请求时候处理
响应拦截器：数据返回之后处理
放在api文件夹下

接口统一管理
项目小，在组件生命周期内发送请求
项目大，统一管理

跨域问题
http://localhost:8080/#/home --本地服务器
http://39.98.123.211/ --后台服务器

json，cros，代理

nprogress 使用
npm install --save nprogress


vuex 
集中管理数组


