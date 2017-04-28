#成功运行应用需要的详细步骤

1. [打开首页]( https://felicityky.github.io/Website-Optimization_zh/)
2. 用你的鼠标或者手指点击屏幕




#学生在 index.html 和 views/js/main.js 中对 pizza.html 进行的优化概述

## 对于index.html
* 第14行，为link标签添加asyc属性，去除阻止首页渲染的CSS
* 第23行，为script标签添加async


## 对于views/js/main.js
* 重写了第460行的changePizzaSizes(size)函数，
  * 避免多次使用document.querySelectorAll(".randomPizzaContainer");
  * 避免发生布局抖动，即首先批量获得dx,因为determineDx函数多次访问了style
