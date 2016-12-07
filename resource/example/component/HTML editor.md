# HTML 编辑器
类似文本编辑器
## 语法

    Ext.create('Ext.form.HtmlEditor');
    
## 例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          Ext.onReady(function() {
             Ext.create('Ext.form.HtmlEditor', {
                width: 580,
                height: 250,
                renderTo: document.getElementById('editorId')
             });
          });
       </script>
    </head>
    <body>
       <div id = "editorId"></div>
    </body>
    </html>
    
运行结果：![运行结果](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/Window.bmp)
