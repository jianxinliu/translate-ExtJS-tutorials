# 窗口
当某些事件被触发，窗口弹出。 `Window` 页可以说是一个绑定了诸如按钮、链接、鼠标悬浮等事件的面板
## 语法

    win = new Ext.Window({properties});
    
##  例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          Ext.onReady(function() {
             win = new Ext.Window({
                title:'Email Window',
                layout:'form',
                width:400,
                closeAction:'close',
                target : document.getElementById('buttonId'),
                plain: true,
                items: [{
                   xtype : 'textfield',
                   fieldLabel: 'To'
                },{
                   xtype : 'textfield',
                   fieldLabel: 'CC'
                },{
                   xtype : 'textfield',
                   fieldLabel: 'BCC'
                },{
                   xtype : 'textfield',
                   fieldLabel: 'Subject'
                },{
                   xtype : 'textarea',
                   fieldLabel: 'Email Message'
                }],
                buttons: [{
                   text: 'Save Draft',
                   handler: function(){Ext.Msg.alert('Save Draft', 'Your msg is saved');}
                },{
                   text: 'Send',
                   handler: function(){Ext.Msg.alert('Message Sent', 'Your msg is sent');}
                },{
                   text: 'Cancel',
                   handler: function(){win.close(); Ext.Msg.alert('close', 'Email window is closed');}
                }],
                buttonAlign: 'center',
             });
             Ext.create('Ext.Button', {
                renderTo: Ext.getElementById('buttonId'),
                text: 'Click Me',
                listeners: {
                   click: function() {
                      win.show();
                   }
                }
             });
          });
       </script>
    </head>
    <body>
       <p> Click the button to see window </p>
       <div id = "buttonId"></div>
    </body>
    </html>

运行结果：![运行结果](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/Window.bmp)    
**说明：当点击按钮，窗口弹出**
