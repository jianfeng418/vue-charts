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

...
 data () {
    return {
      msg: 'Welcome to Your vue-charts',
      barData:{
        title:'业绩（单位w）',
        list:[
          {color:'#53b85e',title:'一季度',num:5},
          {color:'#53805e',title:'二季度',num:14},
          {color:'#4efff0',title:'三季度',num:6},
          {color:'#8a94ee',title:'四季度',num:16},
        ]
      },
      percentData:{
        title:'业绩达成率',
        list:[
          {color:'#53b85e',title:'一季度',num:0.15},
          {color:'#53805e',title:'二季度',num:0.84},
          {color:'#4efff0',title:'三季度',num:0.6},
          {color:'#8a94ee',title:'四季度',num:0.76},
        ]
      }
    }
  }
...

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
  <td>默认自动计算</td>
  </tr>
    <tr>
  <td>maxValue</td>
  <td>Number</td>
  <td>y轴最大值</td>
  <td>默认自动计算</td>
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
  <td>图表的名称</td>
  <td></td>
  </tr>
    <tr>
  <td>list</td>
  <td>Array</td>
  <td>数据列表</td>
  <td>包含数据对象的数组，数据对象格式见下表</td>
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

方法说明：
<table>
<tr>
  <td>方法名称</td>
  <td>参数</td>
  <td>返回值</td>
  <td>描述</td>
  </tr>
  <tr>
  <td>draw</td>
  <td></td>
  <td></td>
  <td>重新绘制图表，在数据更新后，可调用该方法实现图表重绘</td>
  </tr>
</table>