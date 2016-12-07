# 表单
## 描述
在大多数 Web 应用中，表单是重要的获取用户数据的组件，比如登录、反馈等需要从用户处得到数据的操作。在创建表单之前，我们要先了解以下什么是 `xtype`。    
`xtype`用来定义 UI 组件的渲染时类型，比如：元素可以是文本（`xtype:'textField'`）、也可以是纯数字的文本框（`xtype:numberfield`）。
### 不同组件的 **xtype**
|xtype|说明|
---|---
|1. **textfield** |**单行文本框**，类的全称是`Ext.Form.Field.Text`|
|2. **textarea**|**多行文本框**,类的全称是 `Ext.form.field.TextArea`|
|3. **displayfield**|**显示区**，类的全称是 `Ext.form.Label`|
|4. **datefield**|**日期**，提供日期选择，类的全名是 `Ext.form.field.Date`|
|5. **button**|**按钮**，全名是 `Ext.button.Button`|
|6. **radiofield**|**单选框**，类的全名是 `Ext.form.field.Radio`。**需要注意的是，多个单选框需要放置在一个容器里才能起作用**，容器的 xtype 是 **fieldcontainer**|
|7. **checkboxfield**|**多选框**，类的全名是 `Ext.form.field.Checkbox`。**需要注意的事情同单选框**|
|8. **combobox**|**下拉列表**，类的全名是 `Ext.form.field.ComboBox`。**需要注意的是，下拉列表的内容需要另外定义一个数据域**|
|9. **timefield**|**时间输入框**，时间的最大值和最小值可自定义，类的全名是 `Ext.form.field.Time`|
|10. **filefield**|**文件选择框（上传文件时使用）**，类的全名是 `Ext.form.field.File`|
|11. **spinnerfield**|**跳跃式数据输入框**，类的全名是 `Ext.form.field.Spinner`|
|12. **numberfield**|**纯数字输入框**，可规定能输入的数值的范围，类的全名是 `Ext.form.field.Number`|
|13. **hiddenfield**|**隐藏域**|

## 表单面板的语法
    Ext.create('Ext.form.Panel');
### 例程

    <!DOCTYPE html>
    <html>
    <head>
       <link href="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/classic/theme-classic/resources/theme-classic-all.css" rel="stylesheet" />
       <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/extjs/6.0.0/ext-all.js"></script>
       <script type="text/javascript">
          Ext.onReady(function() {
             Ext.create('Ext.form.Panel', {
                id: 'newForm',
                renderTo: 'formId',
                border: true,
                width: 600,
                items: [{
                   xtype: 'textfield',
                   fieldLabel: 'Text Field'
                },{
                   xtype: 'displayfield',
                   fieldLabel: 'Display Field'
                },{
                   xtype: 'textarea',
                   fieldLabel: 'Text Area'
                },{
                   xtype: 'datefield',
                   fieldLabel: 'Date picker'
                },{
                   xtype: 'button',
                   text: 'Button'
                },{
                   xtype: 'fieldcontainer',
                   fieldLabel: 'Radio field',
                   defaultType: 'radiofield',
                   defaults: {
                      flex: 1
                   },
                   layout: 'hbox',
                   items: [{
                      boxLabel: 'A',
                      inputValue: 'a',
                      id: 'radio1'
                   },{
                      boxLabel: 'B',
                      inputValue: 'b',
                      id: 'radio2'
                   },{
                      boxLabel: 'C',
                      inputValue: 'c',
                      id: 'radio3'
                   }]
                },{
                   xtype: 'fieldcontainer',
                   fieldLabel: 'Check Box Field',
                   defaultType: 'checkboxfield',
                   items: [{
                      boxLabel: 'HTML',
                      inputValue: 'html',
                      id: 'checkbox1'
                   },{
                      boxLabel: 'CSS',
                      inputValue: 'css',
                      checked: true,
                      id: 'checkbox2'
                   },{
                      boxLabel: 'JavaScript',
                      inputValue: 'js',
                      id: 'checkbox3'
                   }]
                },{
                   xtype: 'hiddenfield',
                   name: 'hidden field ',
                   value: 'value from hidden field'
                },{
                   xtype: 'numberfield',
                   anchor: '100%',
                   fieldLabel: 'Numeric Field',
                   maxValue: 99,
                   minValue: 0
                },{
                   xtype: 'spinnerfield',
                   fieldLabel: 'Spinner Field',
                   step: 6,
                   // 覆写向上步进按钮的事件监听
                   onSpinUp: function() {
                     var me = this;
                     if (!me.readOnly) {
                         var val = me.step; //设置默认值为step的值
                         if(me.getValue() !== '') {
                             val = parseInt(me.getValue().slice(0, -5));//将自动添加到输入框中的 'pack' 去掉，以便对数值进行运算
                         }                          
                         me.setValue((val + me.step) + ' Pack');
                     }
                   },

                   // 覆写向下步进按钮的事件监听
                   onSpinDown: function() {
                     var me = this;
                     if (!me.readOnly) {
                         if(me.getValue() !== '') {
                             val = parseInt(me.getValue().slice(0, -5)); ////将自动添加到输入框中的 'pack' 去掉，以便对数值进行运算
                         }            
                         me.setValue((val - me.step) + ' Pack');
                     }
                   }
                },{
                   xtype: 'timefield',
                   fieldLabel: 'Time field',
                   minValue: '6:00 AM',
                   maxValue: '8:00 PM',
                   increment: 30,
                   anchor: '100%'
                },{
                   xtype: 'combobox',
                   fieldLabel: 'Combo Box',
                   store: Ext.create('Ext.data.Store', {
                            fields: ['abbr', 'name'],
                            data: [{
                               'abbr': 'HTML',
                               'name': 'HTML'
                            },{
                               'abbr': 'CSS',
                               'name': 'CSS'
                            },{
                               'abbr': 'JS',
                               'name': 'JavaScript'
                            }]
                         }),
                   valueField: 'abbr',
                   displayField: 'name'
                },{
                   xtype: 'filefield',
                   fieldLabel: 'File field',
                   labelWidth: 50,
                   msgTarget: 'side',
                   allowBlank: false,
                   anchor: '100%',
                   buttonText: 'Select File...'
                }]
             });
          });
       </script>
    </head>
    <body>
       <div id = "formId"></div>
    </body>
    </html>
    
[这里](https://www.tutorialspoint.com/extjs/components_form.htm)看结果，拉到页尾。
