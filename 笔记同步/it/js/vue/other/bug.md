Component name "" should always be multi-word vue/multi-word-component-names 
```
原因
法检查的时候把不规范的代码(即命名不规范)当成了错误

解决方案
1.更改组件名(这个比较麻烦),也就是重新起个组件名,使其符合命名规范,如: StudentName 或者 student-name
2.修改配置项,关闭语法检查
在项目的根目录找到(没有就创建)vue.config.js文件
{
const { defineConfig } = require('@vue/cli-service')
module.exports = defineConfig({
 lintOnSave:false
})
}
```

‘xxxxx‘ is defined but never used
```
原因
eg

解决方案
在package.json或者.eslintrc.js中找到  eslintConfig  块，在其rules下加入"no-unused-vars": "off"即可
```


porps引用失败
```
原因
注册名错误

解决方案
不要涉及关键字
```

AVOIDED REDUNDANT NAVIGATION TO CURRENT LOCATION
```js
重复路由错误，index.js添加
const originalPush = VueRouter.prototype.push
VueRouter.prototype.push = function push(location) {
    return originalPush.call(this, location).catch(err => err)
}
const originalreplace = VueRouter.prototype.replace
VueRouter.prototype.replace = function replace(location) {
    return originalreplace.call(this, location).catch(err => err)
}
```
