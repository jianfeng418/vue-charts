<template>
  <div class="">
    <button @click='updateBar' style='float:left'>update</button>
    <vue-bar ref='vuebar' :barData='barData' :barWid='50' class='barDiv' style='clear:both'></vue-bar>
    
    <vue-bar ref='perbar' :barData='percentData' :maxValue='1' dataType='percent' :tickValue='0.2' :precision='2' class='barDiv' ></vue-bar> 
    <div class='circleDiv'>
      <vue-circle :circleData='circleData' style='height:300px' centerText='22' :showTip='true' :showLegend='true' ></vue-circle>
    </div>
    <div class='circleDiv' >
      <vue-circle :circleData='perCircleData' style='height:300px' centerText='22%' :showTip='true' :showLegend='true' :centerStyle='cenStyle'></vue-circle>
    </div>
  </div>
</template>

<script>
import vueChart from 'vue-charts-jf'
import Vue from 'vue'
Vue.use(vueChart);
export default {
  name: 'HelloWorld',
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
      },
      circleData:{
        total:23,
        list:[
          {num:8,title:'一季度',color:'#53b85e'},
          {num:3,title:'二季度',color:'#53805e'},
          {num:5,title:'三季度',color:'#4e1ff0'},
          {num:7,title:'四季度',color:'#8a94ee'}
        ]
      },
      perCircleData:{
        total:23,
        list:[
          {num:8,title:'一季度',color:'#53b85e'},
        ]
      },
      cenStyle:{
        fontSize:'24px',
        fontFamily:'sans-serif',
        fontColor:'#999'
      }
    }
  },
  methods:{
      updateBar(){
        this.barData.list = [
          {color:'#53b85e',title:'一季度',num:8},
          {color:'#53805e',title:'二季度',num:12},
          {color:'#4efff0',title:'三季度',num:9},
          {color:'#8a94ee',title:'四季度',num:18}
        ]
        this.percentData.list = [
          {color:'#53b85e',title:'一季度',num:0.35},
          {color:'#53805e',title:'二季度',num:0.74},
          {color:'#4efff0',title:'三季度',num:0.56},
          {color:'#8a94ee',title:'四季度',num:0.86},
        ]
        this.$refs.vuebar.draw();
        this.$refs.perbar.draw();
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}


.barDiv{
  float:left;
  width:500px;
  height:230px;
  margin:60px
}
.circleDiv{
  height:300px;
  width:500px;
  float:left;
  border:1px solid gray;
  margin:60px
}
</style>
