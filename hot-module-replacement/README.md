## Hot Module Replacement

|本期版本|上期版本
|:---:|:---:
`Tue Mar 28 16:45:06 CST 2023` | -

v5|v4 | 备注
:---:|:---:|:---:
`hot`: `only` | `hot` | 开启HMR, 即不要刷新页面
`-` | 	`hotOnly` | 即使HMR失效，也不要自动刷新浏览器

**<https://webpack.js.org/configuration/dev-server/#devserverhot>**

* To enable Hot Module Replacement without page refresh as a fallback in case of build failures, use hot: 'only':
* Since webpack-dev-server v4, HMR is enabled by default. It automatically applies `webpack.HotModuleReplacementPlugin` which is required to enable HMR



```javascript
const webpack = require('webpack');

new webpack.HotModuleReplacementPlugin({
  // Options...
});
```


```js
if(module.hot) {
  // 如果 number 文件发生了变化执行后面的函数
  module.hot.accept('./number', ()=>{
    console.log('ss')
  })
}
```


### 参考资料

* <https://webpack.js.org/guides/hot-module-replacement/>
* <https://webpack.js.org/api/hot-module-replacement/>
* <https://webpack.js.org/concepts/hot-module-replacement/>

