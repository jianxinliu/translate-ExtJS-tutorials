# 提示工具（ToolTip）
当某些事件被触发，在事件源处悬浮以小块提示信息
## 语法

    T1 = new 'Ext.ToolTip'({properties});
    
## 例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          Ext.onReady(function() {
             toolTip = new Ext.ToolTip({       
                id : 'toolTip',
                anchor : 'bottom',
                html : 'This is a basic toolTip',
                title : 'Tool - Tip Title',
                closable : true,
                closeAction : 'hide'
             });
            Ext.create('Ext.Button', {
                renderTo: Ext.getElementById('buttonId'),
                text: 'Hover Me',
                listeners: {
                   mouseover: function() {
                      toolTip.show();
                   }
                }
             });
          });
       </script>
    </head>
    <body>
       <div id = "buttonId"></div>
    </body>
    </html>
    
运行结果：![运行结果](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/ToolTip.bmp)
**说明：将鼠标悬停在按钮上就会显示一个小框**
