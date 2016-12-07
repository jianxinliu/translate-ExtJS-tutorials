# 网格
## 描述
网格是一个显示数据的简单组件，显示的是存在`Ext.data.Store`里的表格式数据的集合。
## 语法

    Ext.create('Ext.grid.Panel',{
     grid properties..
     columns : [Columns]
    });
    
## 例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          // 创建一个数据模型
          Ext.define('StudentDataModel', {
             extend: 'Ext.data.Model',
             fields: [
             {name: 'name', mapping : 'name'},
             {name: 'age', mapping : 'age'},
             {name: 'marks', mapping : 'marks'}
             ]
          });

          Ext.onReady(function(){
             // 数据域
             var myData = [
                { name : "Asha", age : "16", marks : "90" },
                { name : "Vinit", age : "18", marks : "95" },
                { name : "Anand", age : "20", marks : "68" },
                { name : "Niharika", age : "21", marks : "86" },
                { name : "Manali", age : "22", marks : "57" }
             ];
             // 创建第一个网格的数据域
             var gridStore = Ext.create('Ext.data.Store', {
             model: 'StudentDataModel',
             data: myData
             });
             // 创建第一个网格容器
             Ext.create('Ext.grid.Panel', {
                id                : 'gridId',
                store             : gridStore,
                stripeRows        : true,
                title             : 'Students Grid', //网格的标题
                renderTo          :'gridDiv', //网格渲染到的 div 标签的 id 
                width             : 600,
                collapsible       : true, // 设置为可折叠的网格
                enableColumnMove  :true, // 允许横向拖动滑杆
                enableColumnResize:true, // 允许横向改变大小
                columns           :
                   [{ 
                      header: "Student Name",
                      dataIndex: 'name',	
                      id : 'name',    
                      flex:  1,  		 // 定义此网格在这个网格容器里空间的数量（比例），这一个是1，下面两个都是0.5，则三个网格的横向比例为1:0.5:0.5
                      sortable: true, // 允许对数据排序
                      hideable: true  // 允许此网格隐藏
                   },{
                      header: "Age", 
                      dataIndex: 'age',
                      flex: .5, 
                      sortable: true,
                       hideable: false // 此网格不可隐藏
                   },{
                      header: "Marks",
                      dataIndex: 'marks',
                      flex: .5, 
                      sortable: true, 
                      //渲染器是用来根据条件操作数据显示的，此处分数大于75分则显示Distinction,否则显示Non Distinction
                      renderer :  function (value, metadata, record, rowIndex, colIndex, store) {
                         if (value > 75) {
                            return "Distinction";	  
                         } else {
                            return "Non Distinction";
                         }
                      }
                }]
             });
          });
       </script>
    </head>
    <body>
       <div id = "gridDiv"></div>
    </body>
    </html>
    
到[这里](https://www.tutorialspoint.com/extjs/components_grid.htm)看运行结果，结果是可以交互的
## 网格的属性（properties）
* **collapsible (可折叠)：**此属性给网格增加可折叠功能，冒号后面是一个布尔型数据，默认是 `false`
* **sorting(排序)：**此属性定义网格中的数据是否可排序，默认为`true`.默认的排序也可以这样写：

    sorters:{
            property:'id',
            direction:'ASC'
            }
            
  此时数据将在数据域里按指定方向，指定数据排序，而不等到渲染到网格后再排序
* **enableColumnResize(允许行改变大小)：**允许行改变宽度
* **Hideable(允许行隐藏)：**默认为 `true`   **注意：**此属性是网格里的行的属性
* **enableColumnMove(允许行移动)：**顾名思义
* **renderer(渲染器)：**此属性能让获得的数据自定义得显示
