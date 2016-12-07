# 进度条
顾名思义
## 语法
一个显示任务进程的消息框

    Ext.MessageBox.show({
       title: 'Please wait',
       msg: 'Loading items...',
       progressText: 'Initializing...',
       width:300,
       progress:true,
       closable:false
    });
    
## 例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          Ext.onReady(function() {    
             function progressBar(v) {
                return function()	{
                   if(v == 10) {
                      Ext.MessageBox.hide();
                      result();
                   } else {
                      var i = v/9;
                      Ext.MessageBox.updateProgress(i, Math.round(100*i)+'% completed');
                   }
                };
             };
             function showProgressBar() {
                for(var i = 1; i < 11; i++){
                   setTimeout(progressBar(i), i*500);
                }
             }
             function result(){
                Ext.Msg.alert('status', 'Process completed succesfully');
             }
             Ext.create('Ext.Button', {
                renderTo: Ext.getElementById('buttonId'),
                text: 'Click Me',
                listeners: {
                   click: function() {
                      Ext.MessageBox.show({
                         title: 'Please wait',
                         msg: 'Loading items...',
                         progressText: 'Initializing...',
                         width:300,
                         progress:true,
                         closable:false
                      });
                      showProgressBar();
                   }
                }
             });
          });
       </script>
    </head>
    <body>
       <p> 点击按钮就可以看见进度条</p>
       <div id = "buttonId"></div>
    </body>
    </html>
    
运行结果： ![运行结果](https://raw.githubusercontent.com/jianxinliu/translate-Ext-JS-tutorials/master/resource/progressBar.bmp)    
**结果说明：按下按钮，出现进度条，一段时间后，进度完成**
