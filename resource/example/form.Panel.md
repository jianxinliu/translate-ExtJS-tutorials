# 表单式面板
## 描述
表单式面板为表单提供一个标准的容器，这是一个能为任何`Ext.form.field.Field`对象自动创建 `BasicForm` 管理器的面板类。
## 语法
**语法示例**

    Ext.create('Ext.form.Panel', {
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
             var child1 = Ext.create('Ext.Panel',{     
                html: 'Text field' 
             });

             var child2 = Ext.create('Ext.Panel',{
                html: 'Text field' 
             });
             Ext.create('Ext.form.Panel', {
                renderTo: Ext.getBody(),
                width: 100,
                height : 100,
                border : true,
                frame : true,
                layout: 'auto',// auto is one of the layout type.
                items: [child1, child2]
             });
          });
       </script>
    </head>
    <body>
    </body>
    </html>
    
结果：![结果](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/form.panel.bmp)
