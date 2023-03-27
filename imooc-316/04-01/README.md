# 4-1 Tree Shaking 概念详解

|本期版本|上期版本
|:---:|:---:
`Mon Mar 27 23:20:58 CST 2023` | -

* Tree Shaking 只支持 ES Module
* [`optimization.usedExports`](https://webpack.js.org/configuration/optimization/#optimizationusedexports)


```javascript
import "@babel/polly-fill"
```
```json
"sideEffects": ["@babel/polly-fill"]
"sideEffects": ["*.css"]
```