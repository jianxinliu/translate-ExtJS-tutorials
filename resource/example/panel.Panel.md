# 面板式面板
## 描述
这是允许加到一般面板上的最基本的面板
## 语法
**语法示例**

    Ext.create('Ext.panel.Panel', {
       items: [child1, child2] //这样添加多个子元素作为容器的 item
    });
    
## 例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          Ext.onReady(function () {
             var childPanel1 = Ext.create('Ext.Panel', {
                 html: 'First Panel'
             });

             var childPanel2 = Ext.create('Ext.Panel', {
                 html: 'Another Panel'
             });

             Ext.create('Ext.panel.Panel', {
             renderTo: Ext.getBody(),
                width: 100,
                height : 100,
                border : true,
                frame : true,
                items: [ childPanel1, childPanel2 ]
             });
          });
       </script>
    </head>
    <body>
    </body>
    </html>
    
结果：![结果](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/panel.Panel.bmp)
