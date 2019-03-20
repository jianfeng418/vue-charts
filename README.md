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
使用示例：
```
<vue-bar :barData='barData' :barWid='50' class='barDiv'></vue-bar>

<vue-bar :barData='percentData' :maxValue='1' dataType='percent' :tickValue='0.2' :precision='2' class='barDiv' ></vue-bar>
```

参数说明
<table>
<tr>
  <td>参数名称</td>
  <td>类型</td>
  <td>描述</td>
  <td>默认值</td>
  </tr>
  <tr>
  <td>barData</td>
  <td>Object</td>
  <td>可视化数据源</td>
  <td></td>
  </tr>
    <tr>
  <td>tickValue</td>
  <td>Number</td>
  <td>y轴间隔距离</td>
  <td></td>
  </tr>
    <tr>
  <td>maxValue</td>
  <td>Number</td>
  <td>y轴最大值</td>
  <td></td>
  </tr>
  <tr>
  <td>dataType</td>
  <td>'int' 或者 'percent'</td>
  <td>y轴以整数显示或百分比数显示</td>
  <td>'int'</td>
  </tr>
  <tr>
  <td>precision</td>
  <td>Number</td>
  <td>数据显示的小数点数</td>
  <td>0</td>
  </tr>
  <tr>
  <td>barWid</td>
  <td>Number</td>
  <td>bar图形的宽度</td>
  <td>30</td>
  </tr>
</table>

barData数据格式：
<table>
<tr>
  <td>参数名称</td>
  <td>类型</td>
  <td>描述</td>
  <td>默认值</td>
  </tr>
  <tr>
  <td>title</td>
  <td>String</td>
  <td>图标的名称</td>
  <td></td>
  </tr>
    <tr>
  <td>list</td>
  <td>Array</td>
  <td>数据列表</td>
  <td></td>
  </tr>
</table>

barData.list数据格式：
<table>
<tr>
  <td>参数名称</td>
  <td>类型</td>
  <td>描述</td>
  <td>默认值</td>
  </tr>
  <tr>
  <td>color</td>
  <td>String</td>
  <td>bar图形的颜色</td>
  <td></td>
  </tr>
    <tr>
  <td>title</td>
  <td>String</td>
  <td>bar图形的名称</td>
  <td></td>
  </tr>
  <tr>
  <td>num</td>
  <td>Number</td>
  <td>bar图形的数量</td>
  <td></td>
  </tr>
</table>
