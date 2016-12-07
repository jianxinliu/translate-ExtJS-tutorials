# 图表
图表用来可视化数据， Ext JS 里有如下类型的图表：     
1.[饼状图](https://www.tutorialspoint.com/extjs/piechart.htm):基于极坐标。基本语法：

    Ext.create('Ext.chart.PolarChart', {
     series: [{
       Type: 'pie'
       ..
       }]
       render and other properties.
     });
     
2.[折线图](https://www.tutorialspoint.com/extjs/linechart.htm)：基于笛卡尔坐标。基本语法：

    Ext.create('Ext.chart.CartesianChart',{
       series: [{
          type: 'line',
          xField: 'name',
          yField: 'G1'
          }]
          render, legend and other properties
    });
    
3.[柱状图](https://www.tutorialspoint.com/extjs/barchart.htm)：基于笛卡尔坐标。基本语法：

    Ext.create('Ext.chart.CartesianChart',{
       series: [{
          type: 'bar',
          xField: 'name',
          yField: 'G1'
          }]
          render, legend and other properties
    });
    
4.[折现区域图](https://www.tutorialspoint.com/extjs/areachart.htm)：基于笛卡尔坐标。基本语法：

    Ext.create('Ext.chart.CartesianChart',{
       series: [{
          type: 'area',
          xField: 'name',
          yField: 'G1'
          }]
          render, legend and other properties
    });
    
**注意：请到原文看例程和运行结果**
