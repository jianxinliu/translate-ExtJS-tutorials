# 环境配置
## 在线例子
[传送门](https://www.tutorialspoint.com/extjs/extjs_environment_setup.htm)
## 本地环境配置
#### **注：**原文是6.0版本的环境配置，笔者在此只讲解4.0版本的配置，若读者使用的是6.0版本，请到上方传送门
这部分指导你如何在自己的机器上下载并配置 Ext JS，请按照一下步骤进行：
### 下载库文件
在[sencha](https://www.sencha.com)下载试用版库文件。    
**4.0配置**    
1. 到 Ext Js 4.2目录下下载所有压缩包             
2. spket 是eclipse 下的Ext 插件，有代码提示等功能，插件安装教程网上有很多，读者可自行搜索，**一个重要提示：**将Ext文件、spket文件、eclipse文件放在同一个目录下，可避免一些问题。             
3. 到Ext JS 4.2 目录中的A 文件中找到如下文件，并加入到你的工程中       
* bootstrap.js 启动文件，可以动态选择加载一下几个文件
* ext.js 包含了Ext 的核心功能
* ext-all.js 发布模式下的文件，比以下两个都小
* ext-all-debug.js 测试模式
* ext-all-dev.js 开发模式     
**说明**ext-all.js、ext-all-debug.js、ext-all-dev.js，这三个文件可单独使用，即只在你的工程中加入任意一个即可
* 找到resources\css\ext-all.css               
                   
在一个HTML文件中写如下代码：        
此时，在任意浏览器上浏览这个html文件即可见到效果           
[Try it!](https://www.tutorialspoint.com/extjs/extjs_environment_setup.htm)
