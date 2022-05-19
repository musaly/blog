1. 如何实现一个元素的水平垂直居中
- 绝对定位方法：
```js
.*{
   position: absolute;
   left: 50%;
   top: 50%;
   transform: translate(-50%, -50%);
}
```
- flex 方法：
```js
1.
        .by {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 500px;
            width: 250px;
        }

        .box {
        }
2.
        .by {
            display: flex;
            height: 500px;
            width: 250px;
        }

        .box {
            margin: auto;
        }
```
2. css 如何实现左侧固定 300px，右侧自适应的布局
- flex
```js
.container {
  display: flex;
}

.left {
  flex-basis: 300px;
  flex-shrink: 0;
}

.main {
  flex-grow: 1;
}
```
- Grid 
```js
.container {
  display: grid;
  grid-template-columns: 300px 1fr;
}
```
3. canvas和svg区别















