# vue-charts

> A Vue.js project


![Image message](1.png)

Usage
NPM
```
npm install vue-charts-jf --save
```

```
import vueChart from 'vue-charts-jf'

Vue.use(vueChart);


```
参数说明
<table>
<tr>
  <td>参数名称</td>
  <td>类型</td>
  <td>描述</td>
  </tr>
  <tr>
  <td>event</td>
  <td>Event</td>
  <td>鼠标点击事件</td>
  </tr>
    <tr>
  <td>list</td>
  <td>Array</td>
  <td>下拉菜单数据列表</td>
  </tr>
    <tr>
  <td>ulClass</td>
  <td>String</td>
  <td>为下拉菜单添加的类名</td>
  </tr>
</table>

list数据格式：
<table>
<tr>
  <td>参数名称</td>
  <td>类型</td>
  <td>描述</td>
  </tr>
  <tr>
  <td>icon</td>
  <td>String</td>
  <td>下拉项图标</td>
  </tr>
    <tr>
  <td>text</td>
  <td>String</td>
  <td>下拉项名称</td>
  </tr>
     <tr>
  <td>clickFun</td>
  <td>Function</td>
  <td>下拉项点击响应函数</td>
  </tr>
     <tr>
  <td>disabled</td>
  <td>Boolean</td>
  <td>是否下拉项置灰</td>
  </tr>
</table>

