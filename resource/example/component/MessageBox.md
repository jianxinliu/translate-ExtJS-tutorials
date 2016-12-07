# 消息框
消息框是在某些事件发生时，用来弹出部分信息的组件，有如下几种消息框：

1.[基本警告框](https://www.tutorialspoint.com/extjs/basic_alert_box.htm)alert：最简单的消息框，当某些事件被触发时弹出,基本语法：

    Ext.Msg.alert('Title', 'Basic message box in ExtJS');
 
2.[确认框](https://www.tutorialspoint.com/extjs/confirm_box.htm)confirm：让用户选择确认或者取消，不同的按钮触发不同的函数，基本语法：

    Ext.MessageBox.confirm('Confirm', Msg, optional callbackFunction());

3.[提示框](https://www.tutorialspoint.com/extjs/prompt_box.htm)prompt:让用户确认之前的输入，基本语法：

    Ext.Msg.prompt('Name', 'Please enter your name:', function(){});

4.[多行输入框](https://www.tutorialspoint.com/extjs/multiline_user_input_box.htm)：允许用户输入多行数据，基本语法：

    Ext.MessageBox.show({
       title: 'Details',
       msg: 'Please enter your details:',
       width:300,
       buttons: Ext.MessageBox.OKCANCEL,
       multiline: true,  // 允许多行输入的属性
       fn: callbackFunction
    });
  
5.[确认取消输入框](https://www.tutorialspoint.com/extjs/ync_alert_box.htm)：和确认框类似，但允许更多的操作作为属性加入，基本语法：

    Ext.MessageBox.show({
       title: 'Details',
       msg: 'Please enter your details:',
       width:300,
       buttons: Ext.MessageBox.YESNOCANCEL // this button property for all three options YES, NO, Cancel.
    });
    
**注：请到原文中看例程和运行结果**
