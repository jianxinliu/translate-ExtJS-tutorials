# 表格式面板
## 描述
表格式面板比一般的面板多支持了表格式布局管理器
## 语法
**语法示例**

    Ext.create('Ext.tab.Panel', {
       items: [child1, child2] //这样就可以添加多个子元素到容器中作为 item 
    });    
    
## 例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          Ext.onReady(function () {
             Ext.create('Ext.tab.Panel', {
                renderTo: Ext.getBody(),
                height: 100,
                width: 200,
                items: [{
                   xtype: 'panel',
                   title: 'Tab One',
                   html: 'The first tab',
                   listeners: {
                      render: function() {
                         Ext.MessageBox.alert('Tab one', 'Tab One was clicked.');
                      }
                   }
                   },{
                   // xtype for all Component configurations in a Container
                   title: 'Tab Two',
                   html: 'The second tab',
                   listeners: {
                      render: function() {
                         Ext.MessageBox.alert('Tab two', 'Tab Two was clicked.');
                      }
                   }
                }]
             });
          });
       </script>
    </head>
    <body>
    </body>
    </html>
    
结果截图1：![结果截图1](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/container.Viewport1.bmp)     
结果截图2：![结果截图2](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/container.viewport2.bmp)     
**两张截图的说明：**[原文中](https://www.tutorialspoint.com/extjs/container_tab.htm)页为的结果中的按钮是可按的，按下按钮后会显示不同的结果。
