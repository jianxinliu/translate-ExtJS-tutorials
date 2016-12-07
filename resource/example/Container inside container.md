# 容器中的容器
## 描述
容器嵌套容器，即将一个容器作为组件嵌套进另一个容器。
## 语法
**语法示例**    

     var container = Ext.create('Ext.container.Container', {
          items: [component3, component4]
       });
       Ext.create('Ext.container.Container', {
          renderTo: Ext.getBody(),
          items: [container]
       });
       
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

             var component4 = Ext.create('Ext.Component', {
                html: 'Fourth Component'
             });

             var container = Ext.create('Ext.container.Container', {
                style: {borderStyle: 'solid', borderWidth: '2px' },
                width: '50%',
                items: [component3, component4]
             });

             Ext.create('Ext.container.Container', {
                renderTo: Ext.getBody(),
                title: 'Container',
                border: 1,
                width: '50%',
                style: {borderStyle: 'solid', borderWidth: '2px' },
                items: [component1, component2,  container]
             });
          });
       </script>
    </head>
    <body>
    </body>
    </html>
    
结果：![结果](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/conpReault.bmp)
