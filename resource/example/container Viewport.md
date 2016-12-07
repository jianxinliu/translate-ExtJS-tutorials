# 视图窗口
## 描述
视图窗口是一个根据浏览器窗口大小自动调节大小的容器。也可以嵌入其他 Ext Js 的 UI 组件或容器
## 语法
**语法示例**    

    Ext.create('Ext.container.Viewport', {
       items: [child1, child2] // 这样就可以往容器中加入不同的子组件了
       
## 例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          Ext.onReady(function () {
             var childPanel1 = Ext.create('Ext.panel.Panel', {
                 title: 'Child Panel 1',
                 html: 'A Panel'
             });

             var childPanel2 = Ext.create('Ext.panel.Panel', {
                 title: 'Child Panel 2',
                 html: 'Another Panel'
             });

             Ext.create('Ext.container.Viewport', {
             renderTo: Ext.getBody(),
                 items: [ childPanel1, childPanel2 ]
             });
          });
       </script>
    </head>
    <body>
    </body>
    </html>
    
结果：![结果](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/tab.panel.bmp)

