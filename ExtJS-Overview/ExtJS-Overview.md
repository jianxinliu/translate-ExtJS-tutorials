## 什么是 ExtJS
ExtJS 是一个为桌面应用提供富用户界面的跨浏览器的 JavaScript 流行框架。主要用来建桌面应用，它支持的浏览器有：    
* IE6及以上    
* 火狐    
* Chrome    
* safari6及以上    
* 欧朋（opera）12及以上  ……    
而且 sencha 还有一个移动应用版——sencha touch    
     
ExtJS 是基于 MVC/MVVM 架构，最新版本 Ext JS 6 是一个无需改变代码就能兼容桌面和移动端的独立平台     
## 发展历史
* Ext JS 1.1     
第一个版本是 **Jack Slocum** 在2006年开发的，那时，Ext Js 只是一些基于 YUI 扩展的通用类（YUI extension），那时的名字叫 YUI-ext.（笔者注：这也是Ext JS名字的由来）
* Ext JS 2.0      
2.0版本于2007年发布。这个版本为桌面应用新增了有限功能的 API 文档。**此版本不兼容以前的版本，即不向后兼容**     
* Ext JS 3.0    
3.0版本于2009年发布。此版本新增图表(chart)和列表视图(list view)，但这牺牲了加载速度。**完全向后兼容 2.0版本     
* Ext JS 4.0      
在发布 3.0 以后，Ext JS 的发展面临增速的巨大挑战。 基于此， Ext JS 4.0 在2011年发布。此版本根据 MVC 模式和快速应用的目标，完全修改其结构     
* Ext JS 5.0      
Ext JS 在2014年发布。此版本最大的改变就是将 MVC 架构换成了 MVVM 架构。包含了 1. 兼容可触摸设备和桌面的能力 2. 两个数据绑定的方法 3. 响应式布局 等功能。    
* Ext JS 6.0      
6.0 版本合并了桌面版（Ext JS）和移动版(sencha touch)的框架      
         
## 功能
下面是 Ext JS 一些突出的功能：     
1. 有诸如网格，支点网格(pivot grids)，表单，图表，树 等可定制的 UI 组件。     
2. 向后兼容    
3. 一个有利于跨浏览器、设备和不同尺寸的屏幕之间组织显示数据和内容的灵活的布局管理器     
4. 从数据层将 UI 组件解耦的高级数据包。（Advance data package decouples the UI widgets from the data layer.     
The data package allows client-side collection of data using highly functional models that enable features such as sorting and filtering.）    
5. 这是协议不可知的，所以可以访问任何一种后端资源     
6. 自定义主题的组件跨平台一致性
        
## 优点
sencha 的 Ext JS 引领的商贸 Web 应用开发的标准。它提供了一些编写健壮的桌面和平板应用的必要工具：      
1. 流畅得跨桌面、平板、智能手机三大平台，兼容现代和遗留的浏览器      
2. 通过在企业版开发环境集成 IDE 插件来提高开发团队的效率      
3. 减少 Web 应用的开发成本     
4. 创建极致用户体验的应用     
5. 一堆让用户界面更强大易用的组件      
6. 遵从 MVC 架构的易读代码       
          
## 限制
1. 大至500KB的库文件使得初次加载时间变长，使得应用变慢      
2. 满是 HTML 标签让debug变得困难     
3. 用于开源软件是免费的，用于商业软件则是收费的      
4. 有时用 Ext JS 加载一些东西时的代码量远比纯 HTML 或者 Jquery 的代码量大      
5. 开发 Ext JS 应用需要有经验的开发者          
           
## 工具
sencha 提供了一些产品级的 Ext JS 应用开发工具 
### Sencha Cmd
[Sencha Cmd](http://www.tuicool.com/articles/7niIJf)         
### Sencha IDE Plugins
Sencha IDE Plugins 是集成在 IntelliJ 和 WebStrom IDEs 里的Sencha 框架里的。它提供了诸如代码补全、代码提示、代码导航、代码生成、创建模板、拼写检查等功能来提高开发效率
### Sencha Inspector
一个调试工具
----------------------------
[阅读原文](https://www.tutorialspoint.com/extjs/extjs_overview.htm)
