# 容器中的组件
## 描述
容器中的组件的意思是容器里可以放多个组件
## 语法
**语法示例**

    var component1 = Ext.create('Ext.Component', {
          html:'First Component'
       });
       Ext.create('Ext.container.Container', {
          renderTo: Ext.getBody(),
          items: [component1]
      });
      
将组件作为一个 item 内嵌到容器中。
## 例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          Ext.onReady(function () {
             var component1 = Ext.create('Ext.Component', {
                html:'First Component'
             });

             var component2 = Ext.create('Ext.Component', {
                html: 'Second Component'
             });

             var component3 = Ext.create('Ext.Component', {
                html: 'Third Component'
             });

             Ext.create('Ext.container.Container', {
                renderTo: Ext.getBody(),
                title: 'Container',
                border: 1,
                width: '50%',
                style: {borderStyle: 'solid', borderWidth: '2px' },
                items: [component1, component2,  component3]
             });
          });
       </script>
    </head>
    <body>
    </body>
    </html>
    
结果如下：![结果](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/conResult.bmp)
